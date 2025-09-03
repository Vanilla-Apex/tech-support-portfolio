
# 📄 Case Study: Diagnosing DNS Issues with Public DNS

---

## 🧩 Scenario
A user reported that websites were intermittently failing to load, despite having a stable internet connection. Pages would either timeout or show “DNS server not responding” errors, while other devices on the same network worked fine.

---

## 🔍 Problem
The device was receiving DNS settings automatically from the ISP via DHCP. After testing, I suspected the issue stemmed from the assigned DNS servers being either unreliable or slow to respond.

---

## 🛠️ Steps Taken

1. **Confirmed connectivity:**  
   - Verified the device was connected to the network (pinged local gateway and external IPs like `8.8.8.8`).  
   - Result: Ping success confirmed connectivity, so it wasn’t a hardware or basic networking issue.

2. **Checked current DNS settings:**  
   - Used `ipconfig /all` to view DNS server addresses assigned by the router.  
   - Observed that the DNS was defaulting to the ISP’s DNS servers.

3. **Tested name resolution manually:**  
   - Ran `nslookup google.com` to confirm name resolution delays or failures.  
   - Results were inconsistent, often timing out.

4. **Switched to public DNS manually:**  
   - Changed DNS settings to:
     - **Primary:** 8.8.8.8 (Google)
     - **Secondary:** 1.1.1.1 (Cloudflare)  
   - Modified these under the network adapter’s IPv4 settings.

5. **Flushed DNS cache:**  
   - Ran `ipconfig /flushdns` to clear old records.

6. **Retested browsing and nslookup:**  
   - Websites began loading normally.
   - `nslookup` returned immediate results from public DNS servers.

---

## ✅ Result
Switching to public DNS resolved all browsing issues. The system experienced noticeably faster name resolution and improved website load times.

---

## 🧰 Tools Used
- Command Prompt (`ipconfig`, `nslookup`)
- Windows network adapter settings UI
- Public DNS providers (Google, Cloudflare)

---

## 🧠 What I Learned / Explained to the User
- **DNS can be a hidden bottleneck**—even with perfect connectivity.
- Public DNS servers like Google (`8.8.8.8`) and Cloudflare (`1.1.1.1`) can provide faster and more reliable resolution than default ISP DNS.
- Manually switching DNS can be a quick win for fixing weird connectivity issues.
