
# 🧰 Case Study: USB Device Not Recognized – Registry Fix & Driver Cleanup

---

## 🧩 Scenario
A user connected a USB flash drive that had previously worked, but Windows displayed the error message: **"USB Device Not Recognized."** The drive did not appear in File Explorer or Disk Management.

---

## 🔍 Problem
The device was receiving power (LED light activated), but was not being properly mounted or assigned a drive letter. Device Manager showed a "Unknown USB Device (Device Descriptor Request Failed)" entry. This suggested either a corrupted driver, registry issue, or USB port fault.

---

## 🛠️ Steps Taken

1. **Tested device on other machines:**  
   - Verified that the flash drive worked on another PC.  
   - ✅ Confirmed the issue was isolated to the original machine.

2. **Checked USB root hub power settings:**  
   - In Device Manager → Universal Serial Bus Controllers → USB Root Hub  
   - Disabled the "Allow the computer to turn off this device to save power" setting.

3. **Uninstalled problematic USB drivers:**  
   - In Device Manager, uninstalled the faulty "Unknown USB Device" entry.  
   - Also removed all generic USB mass storage drivers to force a clean reinstall.

4. **Cleaned USB registry entries:**  
   - Opened Registry Editor and navigated to:  
     `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\USB`  
   - Carefully deleted residual keys related to the specific device.

5. **Restarted PC and reconnected device:**  
   - Upon reboot, Windows reinstalled USB controllers and the device was successfully recognized.

---

## ✅ Result
The flash drive was detected properly, assigned a drive letter, and appeared in File Explorer. The user was able to access their files and continue using the device without errors.

---

## 🧰 Tools Used
- Device Manager
- Registry Editor (`regedit`)
- Basic USB diagnostics
- Test on multiple devices

---

## 🧠 What I Learned / Explained to the User
- Corrupted USB registry entries can block device recognition even when hardware is working.
- Cleaning up drivers and registry keys helps Windows force proper reinitialization.
- Always test USB devices on other machines to isolate the problem source.
