
# ⚡ Case Study: How I Used `chkdsk` and `sfc /scannow` to Fix System Corruption

---

## 🧩 Scenario
A user reported that their Windows system was acting unstable: programs were crashing randomly, and Windows updates were failing to install. They had not installed any new software or hardware recently.

---

## 🔍 Problem
The symptoms suggested potential system file corruption or hard disk errors. No malware was detected, and memory passed a basic diagnostic test. It was time to dig deeper using built-in repair tools.

---

## 🛠️ Steps Taken

1. **Opened Command Prompt as Administrator:**  
   - Used `cmd` with elevated privileges to run system repair tools.

2. **Ran System File Checker (SFC):**  
   - Command: `sfc /scannow`  
   - Detected and repaired several corrupted or missing system files.  
   - Prompted for a reboot to complete some repairs.

3. **Ran Check Disk Utility (CHKDSK):**  
   - Command: `chkdsk C: /f /r`  
   - Scheduled to run on next reboot.  
   - After restart, disk sectors were scanned and some bad clusters were repaired.

4. **Verified system health post-repair:**  
   - Checked Event Viewer logs to confirm repair events.  
   - Re-attempted failed Windows update—this time it succeeded.  
   - Programs no longer crashed during normal use.

---

## ✅ Result
The combination of `sfc /scannow` and `chkdsk` repaired the system without needing a reset or reinstall. The user’s PC returned to a stable state with no recurring issues.

---

## 🧰 Tools Used
- Command Prompt (Admin)
- `sfc /scannow`
- `chkdsk /f /r`
- Event Viewer (for confirmation)

---

## 🧠 What I Learned / Explained to the User
- Windows includes powerful, underused tools to repair corruption.
- Running SFC and CHKDSK can resolve serious issues without touching user data.
- It's important to run these with elevated permissions and understand how to read the results.
