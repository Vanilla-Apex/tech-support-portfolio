# 🛠️ Linux Permission Fix on Ubuntu (chmod / chown)

## 🔧 Summary
A user on an Ubuntu system was unable to execute scripts and access files within a specific directory, despite the files being present and readable by other users.  
This case study covers diagnosing Linux file permissions, identifying incorrect ownership and mode settings, and restoring correct access using `chmod` and `chown`.

---

## 🔍 Symptoms

- User received “Permission denied” when executing a script  
- Files were visible but could not be modified or run  
- Same files worked correctly when accessed by another user  
- Issue persisted after reboot  
- No filesystem errors present  

---

## 🔎 Diagnostics Performed

### 1. Verified File Permissions
Listed file permissions using:

    ls -l

Observed:
- Execute bit missing on script file  
- Directory owned by root instead of the user  
- User belonged to correct group but lacked ownership  

### 2. Checked Directory Permissions
Inspected parent directory permissions:

    ls -ld /path/to/directory

- Directory required execute permission for traversal  
- Ownership mismatch prevented access  

### 3. Confirmed User and Group Membership

    whoami
    groups

- User was not the owner of the files  
- Group permissions were insufficient  

This confirmed the issue was **permission and ownership related**, not application or filesystem corruption.

---

## 🔧 Resolution

### 1. Changed File Ownership
Assigned ownership of files and directories to the correct user and group:

    sudo chown -R username:groupname /path/to/directory

### 2. Restored Execute Permission on Script
Added execute permission for the owner:

    chmod u+x script.sh

### 3. Corrected Directory Permissions
Ensured directory allowed user access and traversal:

    chmod 755 /path/to/directory

### 4. Verified Permissions
Rechecked permissions:

    ls -l
    ls -ld /path/to/directory

- Ownership correctly assigned  
- Execute permission restored  
- User could access and run files normally  

---

## 🧩 Root Cause
Files and directories were created or copied using elevated privileges, resulting in root ownership and restrictive permissions.  
This prevented the intended user from executing scripts or modifying files.

Correcting ownership and permission bits resolved the issue.

---

## 📘 Skills Demonstrated

- Linux file permission analysis  
- Understanding of read/write/execute bits  
- Ownership vs permission troubleshooting  
- Safe use of `chmod` and `chown`  
- Command-line diagnostics  
- Explaining Linux permissions clearly to users  

---

## 🧰 Tools & Commands Used

    ls -l
    ls -ld
    whoami
    groups
    chmod
    chown
    sudo

---

## 🛡️ Preventative Measures

- Avoid using sudo unnecessarily when creating user files  
- Verify ownership after copying files from root locations  
- Use group permissions carefully for shared directories  
- Apply the principle of least privilege  

---

## ✅ Final Outcome
After correcting file ownership and permissions, the user was able to access and execute files normally.  
The system returned to expected behavior with no further permission errors reported.
