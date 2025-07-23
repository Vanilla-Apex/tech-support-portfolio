# ⚙️ Mini Project: Automating Temp File Cleanup with a Windows Batch File

## 🎯 Purpose

To automate the process of cleaning up temporary files in Windows using a batch script, reducing system clutter and improving performance.

---

## 💻 Script Details

- Deletes files in the following locations:
  - Windows Temp folder
  - Current user Temp folder
- Requests admin privileges
- Provides confirmation messages to the user

---

## 📄 Script Code

```batch
@echo off
echo Cleaning temporary files...
del /s /q %temp%\*.*
del /s /q C:\Windows\Temp\*.*
echo Temp file cleanup complete.
pause
```

---

## 🪜 Steps Taken

1️⃣ Opened Notepad and wrote the batch file commands  
2️⃣ Saved the file as `cleanup_temp.bat`  
3️⃣ Right-clicked the file and selected “Run as administrator”  
4️⃣ Observed confirmation messages and verified cleanup  
5️⃣ Scheduled for monthly use with Task Scheduler (optional step)

---

## ✅ Outcome

- Successfully cleared temp folders in seconds
- Reduced system clutter and freed up several hundred MB of disk space
- Useful tool for basic PC maintenance and end-user support

---

## 💡 Skills Practiced

- Scripting and automation with batch files
- Windows file path and permissions management
- Maintenance-focused technical support
