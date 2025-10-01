
# 🖥️ Case Study: Fixing a “No Boot Device Found” Error (UEFI/BIOS Settings)

---

## 🧩 Scenario
After a user restarted their laptop, the system failed to boot and displayed the error:  
**“No Boot Device Found. Press any key to reboot the machine.”**  
The user hadn’t made any recent hardware changes or OS reinstalls.

---

## 🔍 Problem
The BIOS/UEFI settings had reset to default, possibly due to a low CMOS battery or abrupt shutdown. As a result, the boot mode was set to UEFI, but the drive had a legacy (MBR) installation, or vice versa. In other cases, the internal drive was disabled in BIOS or not prioritized correctly in the boot order.

---

## 🛠️ Steps Taken

1. **Verified physical connections:**  
   - Confirmed SSD was detected by reseating and checking connections (if desktop).  
   - For laptops, confirmed drive presence in BIOS.

2. **Entered BIOS/UEFI Setup:**  
   - Pressed appropriate key during boot (e.g., F2, DEL, ESC depending on brand).  
   - Navigated to boot settings and checked for storage devices.

3. **Checked boot mode compatibility:**  
   - Verified if OS was installed in Legacy (MBR) or UEFI (GPT) mode.  
   - Switched boot mode in BIOS to match installation type.

4. **Enabled storage controller & drive:**  
   - In some BIOS setups, the drive was disabled or the storage controller (SATA/RAID/AHCI) was incorrectly set.

5. **Adjusted boot order:**  
   - Made sure the internal SSD or HDD was listed as the first boot device.

6. **Saved changes and rebooted:**  
   - System successfully booted into Windows.

---

## ✅ Result
The “No Boot Device Found” error was resolved by aligning BIOS settings with the installed OS configuration and restoring the correct boot priority. No data loss occurred, and no reinstallation was necessary.

---

## 🧰 Tools Used
- BIOS/UEFI firmware interface
- OS knowledge: UEFI vs Legacy
- Optional: Bootable USB to confirm drive visibility (not needed in this case)

---

## 🧠 What I Learned / Explained to the User
- Boot mode mismatches can prevent startup even when drives are healthy.
- BIOS resets can happen silently and lead to major confusion for end users.
- Knowing how to navigate BIOS and identify boot drive issues is an essential support skill.
