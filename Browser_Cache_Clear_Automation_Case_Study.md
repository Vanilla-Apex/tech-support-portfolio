
# 🧹 Automating Browser Cache Clear with Task Scheduler + Script

---

## 🧩 Scenario  
In shared environments like classrooms or multi-user PCs, browsers can quickly accumulate cache and temp data, leading to sluggish performance or profile glitches. Rather than relying on users to manually clear this, I automated the cleanup process using Task Scheduler and scripting.

---

## 🔍 Problem  
Users were experiencing slow browser performance, occasional website loading issues, and login conflicts — all tied to leftover cache and cookies. Manual clearing was inconsistent and not scalable in a shared device setting.

---

## 🛠️ Steps Taken

1. **Designed a cleanup script**  
    - Created a batch file and PowerShell script combo to silently delete browser cache for Chrome and Edge.

2. **Identified browser cache paths**  
    - Chrome: `%LOCALAPPDATA%\Google\Chrome\User Data\Default\Cache`  
    - Edge: `%LOCALAPPDATA%\Microsoft\Edge\User Data\Default\Cache`

3. **Used PowerShell to remove contents**  
    ```powershell
    Remove-Item "$env:LOCALAPPDATA\Google\Chrome\User Data\Default\Cache\*" -Force -Recurse
    Remove-Item "$env:LOCALAPPDATA\Microsoft\Edge\User Data\Default\Cache\*" -Force -Recurse
    ```

4. **Wrapped the cleanup in a `.bat` script**  
    - This allowed it to be triggered by Task Scheduler.

5. **Created a Task Scheduler job**  
    - Trigger: “At log on” for all users  
    - Action: Run the `.bat` script  
    - Settings: Run with highest privileges, hidden window

6. **Tested across multiple profiles**  
    - Verified successful silent cleanup post-login without user intervention

---

## ✅ Result  
Browser performance improved, and users no longer experienced the same sluggishness or login issues. Automation ensures consistency and reduces support requests.

---

## 🧰 Tools Used  
- PowerShell  
- Batch scripting  
- Task Scheduler (Windows)  
- Local file system permissions

---

## 🧠 What I Learned  
- Task Scheduler is a powerful but underused tool in desktop support  
- A combination of scripting and automation can reduce long-term support friction  
- Understanding file paths and permissions is key when working across user accounts

