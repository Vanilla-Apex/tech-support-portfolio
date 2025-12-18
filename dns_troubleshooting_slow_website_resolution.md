# 🛠️ DNS Troubleshooting for Slow Website Resolution

## 🔧 Summary
A user reported that websites were loading slowly despite having a stable internet connection and normal download speeds.  
Initial tests showed that pages eventually loaded, but name resolution was noticeably delayed.  
This case study covers diagnosing DNS-related latency, testing public DNS providers, flushing local caches, and applying router-level fixes.

---

## 🔍 Symptoms

- Websites took several seconds to begin loading  
- Downloads and streaming speeds were normal once pages loaded  
- Issue affected multiple browsers  
- Problem persisted across different websites  
- Restarting the PC provided only temporary improvement  

---

## 🔎 Diagnostics Performed

### 1. Verified Network Connectivity
Confirmed general connectivity was healthy:

    ping 8.8.8.8

- Stable replies with low latency  
- No packet loss  
- Indicated internet connection itself was not the issue  

### 2. Tested DNS Resolution Speed
Tested name resolution using ping with domain names:

    ping google.com

- Initial delay before resolving hostname  
- Subsequent pings resolved faster (cached)  

This suggested DNS lookup delay rather than bandwidth issues.

### 3. Checked Current DNS Configuration

    ipconfig /all

- System was using ISP-provided DNS servers  
- No custom DNS entries configured  
- Multiple network devices on same router affected  

### 4. Flushed Local DNS Cache

    ipconfig /flushdns

- Temporary improvement observed  
- Issue returned after extended use  

This indicated the problem was upstream of the local machine.

---

## 🔧 Resolution

### 1. Tested Public DNS Providers
Manually set DNS servers on the network adapter for testing.

Cloudflare DNS:

    Preferred DNS: 1.1.1.1
    Alternate DNS: 1.0.0.1

Google DNS:

    Preferred DNS: 8.8.8.8
    Alternate DNS: 8.8.4.4

- Websites began resolving immediately  
- Noticeable improvement in first-page load times  
- Issue resolved across all browsers  

### 2. Applied Router-Level DNS Fix
Logged into the router admin interface:

- Changed router DNS from ISP default to Cloudflare DNS  
- Ensured all connected devices inherited new DNS settings via DHCP  
- Rebooted router to apply changes  

### 3. Renewed Client Network Configuration

    ipconfig /release
    ipconfig /renew

- Confirmed clients received updated DNS settings  
- Verified with ipconfig /all  

---

## 🧩 Root Cause
The ISP-provided DNS servers were responding slowly to DNS queries, causing delayed hostname resolution.  
Once a site resolved, performance was normal — masking the true cause.

Switching to faster, more reliable public DNS servers eliminated the latency.

---

## 📘 Skills Demonstrated

- DNS troubleshooting methodology  
- Differentiating bandwidth vs name resolution issues  
- Using ipconfig for network diagnostics  
- Testing and comparing public DNS providers  
- Router-level configuration changes  
- Explaining networking concepts to non-technical users  

---

## 🧰 Tools & Commands Used

    ping
    ipconfig /all
    ipconfig /flushdns
    ipconfig /release
    ipconfig /renew
    Router admin interface
    Public DNS services (Cloudflare / Google)

---

## 🛡️ Preventative Measures

- Use reliable public DNS providers when ISP DNS is slow  
- Reboot router periodically to clear stale cache  
- Flush DNS cache when browsing issues appear  
- Keep router firmware updated  

---

## ✅ Final Outcome
After switching DNS resolution to Cloudflare and applying the change at the router level, website load times improved immediately.  
The issue was resolved across all devices on the network, and browsing performance returned to normal.
