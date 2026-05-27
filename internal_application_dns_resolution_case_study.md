# 🛠️ Internal Application Failure Caused by DNS Resolution Issue

---

## 🔧 Summary

Users reported being unable to access an internal application despite the server remaining online and network connectivity appearing normal.

This case study covers diagnosing DNS-related service failures by verifying connectivity, testing name resolution, and restoring access after correcting DNS configuration.

---

## 🔍 Symptoms

- Internal application unavailable to users  
- Server responding to connectivity tests  
- IP-based access functioning normally  
- Hostname-based access failing  
- Other services operating as expected  

---

## 🔎 Diagnostics Performed

### 1. Verified network connectivity

- Confirmed server responded to connectivity tests  
- Verified no packet loss or network outage  
- Ensured system remained reachable  

### 2. Tested application access

- Attempted access using hostname  
- Confirmed hostname failed to resolve correctly  
- Retested using direct IP address  
- Verified application loaded successfully via IP  

### 3. Checked DNS configuration

- Reviewed configured DNS settings  
- Verified active DNS server assignments  
- Observed incorrect name resolution responses  

### 4. Performed name resolution testing

- Tested hostname lookup  
- Compared results against expected records  
- Confirmed DNS mismatch affecting application access  

### 5. Corrected DNS configuration

- Updated DNS settings  
- Cleared cached DNS entries  
- Verified correct hostname resolution  

### 6. Retested application availability

- Accessed application using hostname  
- Confirmed successful connection  
- Verified normal operation restored  

---

## ✅ Result

After correcting DNS configuration and clearing cached entries, hostname resolution functioned normally and application access was restored.

---

## 🧰 Tools Used

- nslookup (DNS testing)  
- ping (connectivity testing)  
- DNS configuration tools  
- Application access testing  

---

## 🧠 What I Learned / Explained to the User

- Connectivity and DNS are separate troubleshooting layers  
- Successful ping tests do not always confirm application availability  
- Hostname failures can isolate DNS-related issues quickly  
- Clearing cached records can help restore normal resolution behavior
