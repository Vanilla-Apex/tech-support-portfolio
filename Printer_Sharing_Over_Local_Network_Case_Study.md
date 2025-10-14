
# 🖨️ Case Study: Sharing a Printer Across a Local Network (Home Network Use Case)

---

## 🧩 Scenario
A home user had a printer connected to a desktop PC via USB but wanted to print from a second laptop on the same Wi-Fi network without buying a network printer or additional hardware.

---

## 🔍 Problem
The printer was not network-enabled, and the laptop couldn't detect it. Printer sharing had not been set up, and Windows Firewall was blocking discovery.

---

## 🛠️ Steps Taken

1. **Verified both devices were on the same network:**  
   - Ensured desktop and laptop were connected to the same Wi-Fi router/subnet.

2. **Enabled printer sharing on the desktop:**  
   - Opened Control Panel → Devices and Printers  
   - Right-clicked the printer → Printer Properties → Sharing tab  
   - Checked "Share this printer" and gave it a recognizable name

3. **Allowed network discovery and file/printer sharing:**  
   - Control Panel → Network and Sharing Center → Advanced sharing settings  
   - Enabled network discovery and file/printer sharing for private networks

4. **Checked firewall settings:**  
   - Opened Windows Defender Firewall → Allowed apps  
   - Ensured "File and Printer Sharing" was enabled for private networks

5. **Connected the shared printer from the laptop:**  
   - Went to Control Panel → Devices and Printers → Add a Printer  
   - Selected "The printer that I want isn’t listed" → "Select a shared printer by name"  
   - Entered the shared path (e.g., `\\DESKTOP-PC\Canon_Printer`)

6. **Installed drivers if prompted:**  
   - Windows automatically installed compatible drivers from the desktop or prompted for download

---

## ✅ Result
The laptop was successfully able to send print jobs to the printer connected to the desktop. Both devices remained stable, and the setup worked across reboots.

---

## 🧰 Tools Used
- Windows Control Panel
- Network and Sharing Center
- Windows Defender Firewall
- Printer Properties and local device settings

---

## 🧠 What I Learned / Explained to the User
- USB printers can be shared across a home network without needing a print server or special hardware.
- Proper configuration of sharing settings and firewall rules is key.
- Using descriptive printer share names helps reduce confusion on multi-device networks.
