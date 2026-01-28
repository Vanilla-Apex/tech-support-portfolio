# 🛠️ Case Study: Linux Service Fails to Start on Boot Due to systemd Unit Misconfiguration

---

## 🔧 Summary

A Linux system reported that a required service was not running after reboot, despite being enabled and functioning correctly when started manually. The issue caused dependent applications to fail silently at startup.

This case study covers diagnosing service startup failures caused by misconfigured systemd unit files and restoring reliable service initialization during system boot.

---

## 🔍 Symptoms

- Service was not running after system reboot  
- Dependent applications failed to start automatically  
- Manually starting the service succeeded without errors  
- No obvious failure messages were shown to the user  
- Issue persisted across multiple reboots  

---

## 🧪 Diagnostics Performed

### 1. Verified Service Status
- Checked service status using `systemctl status`  
- Confirmed the service was inactive after boot  
- Verified the service was enabled  

### 2. Tested Manual Service Start
- Started the service manually using `systemctl start`  
- Confirmed the service started successfully  
- Result: Service itself was functional  

### 3. Reviewed Boot Logs
- Inspected boot and service logs using `journalctl`  
- Identified timing-related errors during startup  
- Noted missing or unmet startup conditions  

### 4. Inspected systemd Unit Configuration
- Reviewed the service unit file  
- Identified incorrect or missing dependency directives  
- Confirmed the service was starting before required targets were available  

### 5. Corrected Startup Configuration
- Updated the unit file to include proper dependency and ordering directives  
- Reloaded systemd configuration  
- Rebooted the system to validate changes  

---

## ✅ Resolution

Correcting the systemd unit configuration ensured the service started at the appropriate point during system boot. After the fix, the service initialized reliably on every reboot, and dependent applications functioned as expected.

---

## 🧰 Tools Used

- `systemctl`  
- `journalctl`  
- systemd unit file inspection  

---

## 🧠 What I Learned / Explained to the User

- A service can be enabled but still fail to start correctly at boot  
- Manual startup success does not guarantee correct boot-time behavior  
- systemd startup order and dependencies are critical for reliable services  
- Reviewing boot logs is essential when diagnosing startup-related issues  
