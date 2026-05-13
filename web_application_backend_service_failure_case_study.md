# 🛠️ Web Application Unreachable Due to Failed Backend Service

---

## 🔧 Summary

Users reported being unable to access a web application hosted on an internal server. The application webpage failed to load despite the server remaining online and reachable on the network.

This case study covers diagnosing application availability issues by verifying server connectivity, isolating backend service failures, and restoring normal functionality.

---

## 🔍 Symptoms

- Web application inaccessible to users  
- Browser returned connection or loading errors  
- Server responding to network connectivity checks  
- Other services on the server functioning normally  
- Issue isolated to a single application  

---

## 🔎 Diagnostics Performed

### 1. Verified server connectivity

- Confirmed the server responded to network connectivity tests  
- Verified the system was reachable on the network  
- Ensured no general network outage was present  

### 2. Tested web application access

- Attempted access from multiple devices  
- Confirmed application consistently failed to load  
- Determined issue was not browser-specific  

### 3. Reviewed service status

- Checked status of backend application service  
- Confirmed required service was inactive  
- Observed failure during startup attempts  

### 4. Reviewed system logs

- Checked logs related to the failed service  
- Identified dependency-related startup error  
- Determined supporting backend process was not running  

### 5. Restarted dependent services

- Restarted required backend dependency  
- Restarted affected web application service  
- Confirmed services initialized successfully  

### 6. Retested application access

- Reloaded application from multiple devices  
- Verified successful application access  
- Confirmed normal functionality restored  

---

## ✅ Result

After restoring the failed backend dependency and restarting the affected service, the web application became accessible again and normal operation resumed.

---

## 🧰 Tools Used

- systemctl (service management)  
- journalctl / application logs  
- Network connectivity testing  
- Web browser  

---

## 🧠 What I Learned / Explained to the User

- Application outages are not always caused by server downtime  
- Services may depend on supporting backend processes to function correctly  
- Verifying connectivity separately from application availability helps isolate issues  
- Logs and service status checks are critical for diagnosing server-side failures  
