# 🛠️ Case Study: DNS Resolution Delays Caused by Stale Cache and TTL Mismatch

---

## 🔧 Summary

A user reported that specific websites were consistently slow to load on one device, while other websites and devices on the same network performed normally. Pages eventually loaded, but name resolution was noticeably delayed rather than failing outright.

This case study covers diagnosing DNS-related latency caused by stale cached records and mismatched Time To Live (TTL) values, and resolving the issue by validating resolver behavior and switching DNS providers.

---

## 🔍 Symptoms

- Websites took several seconds to begin loading  
- Pages eventually loaded successfully  
- Download and streaming speeds were normal  
- Issue affected multiple browsers  
- Problem persisted across different websites  
- Restarting the system provided only temporary improvement  

---

## 🧪 Diagnostics Performed

### 1. Verified Network Connectivity
- Confirmed access to the local gateway  
- Successfully pinged external IP addresses (e.g. `8.8.8.8`)  
- Result: Network connectivity was stable  

### 2. Tested DNS Resolution Timing
- Ran `nslookup` against affected domains  
- Observed delayed responses despite successful resolution  
- Compared resolution timing with unaffected domains  

### 3. Identified Active DNS Resolver
- Confirmed the system was receiving DNS settings via DHCP  
- Determined the ISP-provided DNS servers were in use  

### 4. Tested DNS Cache Behavior
- Flushed the local DNS cache using `ipconfig /flushdns`  
- Retested DNS resolution immediately after cache clearance  
- Observed temporary improvement in resolution speed  

### 5. Compared Public DNS Providers
- Manually configured DNS settings:
  - Primary: `8.8.8.8` (Google)  
  - Secondary: `1.1.1.1` (Cloudflare)  
- Retested name resolution using `nslookup`  

---

## ✅ Resolution

Switching to public DNS resolvers eliminated the resolution delays. DNS queries returned immediately, and affected websites loaded consistently without lag.

---

## 🧰 Tools Used

- Command Prompt (`ping`, `nslookup`, `ipconfig /flushdns`)  
- Windows network adapter IPv4 settings  
- Public DNS providers (Google, Cloudflare)  

---

## 🧠 What I Learned / Explained to the User

- DNS issues can cause noticeable delays without breaking connectivity  
- Stale cached records and TTL mismatches can degrade browsing performance  
- Flushing the DNS cache may temporarily mask the issue  
- Switching to reliable public DNS resolvers can provide a consistent long-term fix  
