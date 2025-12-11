# 🛠️ Fixing a Broken GPU Driver Causing a Black Screen

## 🔧 Summary
A Windows 10 PC was booting to a black screen — no display, no cursor, no response — although system sounds indicated Windows was loading in the background.  
The root cause was a corrupted GPU driver preventing normal display initialization.  
This case study covers booting into Safe Mode, using DDU (Display Driver Uninstaller) to remove the faulty driver, and performing a clean reinstall.

---

## 🔍 Symptoms

- System boots to a black screen after the Windows logo  
- Monitor shows “No Signal” intermittently  
- Keyboard shortcuts like Ctrl + Alt + Del produce sound but no visual changes  
- Safe Mode works, confirming hardware is functional  
- Recent forced shutdown or update prior to issue  

---

## 🔎 Diagnostics Performed

### 1. Verified Hardware Output
- Confirmed monitor and cable functioning with another device  
- Tried alternate GPU output ports  
- Confirmed PC boots (Windows startup sounds played)

### 2. Booted Into Safe Mode
Entered Windows Safe Mode using Shift + Restart:

    shutdown /r /o /f /t 00

From Safe Mode:
- Display output worked normally  
- Device Manager showed GPU driver with warnings  

This confirmed **driver-level failure**, not hardware damage.

### 3. Checked System Logs
Using Event Viewer → System:

- Display driver initialization failures  
- Kernel-PnP errors related to GPU  
- No hardware faults  

---

## 🔧 Resolution

### 1. Booted Into Safe Mode (with Networking)

    Press Shift while selecting Restart  
    Troubleshoot  
    Advanced Options  
    Startup Settings  
    Enable Safe Mode with Networking

### 2. Downloaded Display Driver Uninstaller (DDU)
Downloaded the latest DDU version from Wagnardsoft.

### 3. Removed Faulty GPU Driver Using DDU
Inside Safe Mode:

    Launched DDU  
    Selected GPU device type (NVIDIA/AMD/Intel)  
    Chose “Clean and Restart”  

DDU removed:
- Corrupt GPU driver  
- Leftover registry entries  
- Old profiles and cached configs  

### 4. Performed Clean GPU Driver Installation
After reboot into normal mode:

    Installed the latest WHQL GPU driver from manufacturer website

### 5. Reboot and Verification
- Display output restored  
- Resolution and refresh rate detected correctly  
- Device Manager showed a normal GPU entry  
- No further errors in Event Viewer  

---

## 🧩 Root Cause
A corrupted GPU driver prevented Windows from initializing the graphics subsystem during normal boot.  
Safe Mode bypassed the faulty driver, confirming software-level failure.  
DDU fully removed the broken installation and allowed a clean reinstall.

---

## 📘 Skills Demonstrated

- Booting into Safe Mode for diagnostics  
- Using DDU safely and correctly  
- Understanding GPU driver initialization  
- Troubleshooting black-screen failures  
- Verifying hardware vs software failures  
- Reading Event Viewer logs  
- Clear escalation and rollback planning  

---

## 🧰 Tools & Commands Used

    shutdown /r /o /f /t 00
    DDU (Display Driver Uninstaller)
    Device Manager
    Event Viewer
    WHQL GPU driver installer

---

## 🛡️ Preventative Measures

- Avoid forced shutdowns during driver updates  
- Keep GPU drivers updated to WHQL-stable builds  
- Use manufacturer installers, not Windows Update  
- Create a restore point before major driver changes  

---

## ✅ Final Outcome
After removing the corrupted GPU driver with DDU and performing a clean reinstall, the system’s display output was restored.  
Windows booted normally, GPU functions were fully available, and no further black-screen issues occurred.

