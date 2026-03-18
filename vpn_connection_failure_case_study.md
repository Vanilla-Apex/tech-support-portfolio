# 🛠️ User Unable to Connect to VPN

---

## 🔧 Summary

A user reported being unable to connect to the corporate VPN while working remotely. The VPN client failed to establish a connection, preventing access to internal resources.

This case study covers diagnosing VPN connectivity issues by verifying network access, validating credentials, and isolating client-side configuration problems.

---

## 🔍 Symptoms

- VPN client unable to establish connection  
- Error message displayed during connection attempt  
- User unable to access internal company resources  
- Internet connection functioning normally  
- Issue isolated to a single user  

---

## 🔎 Diagnostics Performed

### 1. Verified basic internet connectivity

- Confirmed the user could access external websites  
- Verified stable internet connection  
- Ensured no general network outages were present  

### 2. Checked VPN client status

- Confirmed VPN client application was installed and up to date  
- Restarted the VPN client to rule out temporary issues  
- Attempted reconnection  

### 3. Validated user credentials

- Confirmed username and password were entered correctly  
- Asked the user to re-enter credentials  
- Verified account was not locked or expired  

### 4. Tested DNS and network reachability

- Confirmed VPN server address could be resolved  
- Used basic connectivity checks to ensure the server was reachable  
- Verified no local network restrictions were blocking the connection  

### 5. Reviewed client configuration

- Checked VPN profile settings  
- Identified incorrect server configuration in the client  
- Corrected the VPN server address  

### 6. Retested VPN connection

- Attempted connection after correcting configuration  
- VPN connected successfully  
- Verified access to internal resources  

---

## ✅ Result

After correcting the VPN client configuration, the user successfully connected to the VPN and regained access to internal systems.

---

## 🧰 Tools Used

- VPN client software  
- Web browser  
- Network connectivity checks  
- DNS resolution  

---

## 🧠 What I Learned / Explained to the User

- VPN issues are often caused by configuration errors rather than network failure  
- Verifying basic connectivity helps isolate the problem quickly  
- Correct server settings are critical for successful VPN connections  
- Systematic troubleshooting prevents unnecessary escalation  
