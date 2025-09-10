
# 🔋 Case Study: Replacing a Laptop Battery (and Testing It Safely)

---

## 🧩 Scenario
A user reported that their laptop was shutting down unexpectedly when unplugged, even though the battery indicator still showed a partial charge. The issue persisted across multiple usage sessions.

---

## 🔍 Problem
Battery wear and capacity degradation were suspected. The laptop's battery was original and over 3 years old, and symptoms pointed to diminished charge retention or incorrect battery reporting.

---

## 🛠️ Steps Taken

1. **Reviewed system battery reports:**  
   - On Windows, ran `powercfg /batteryreport` to generate a detailed battery health report.
   - Compared **design capacity** vs **full charge capacity**.

2. **Verified hardware condition visually:**  
   - Inspected battery for swelling, wear, or physical damage.
   - Battery was not swollen but showed signs of aging.

3. **Removed old battery safely:**  
   - Powered off and disconnected laptop from power.
   - Used anti-static strap and tools to open the laptop and remove the battery.

4. **Installed new OEM-compatible battery:**  
   - Inserted replacement and secured connections.
   - Reassembled the laptop and charged battery to 100%.

5. **Retested battery performance:**  
   - Confirmed the laptop remained stable on battery power.
   - Re-ran `powercfg /batteryreport` to validate full charge capacity improvements.

---

## ✅ Result
The battery replacement resolved the unexpected shutdowns. The new battery showed over 95% of design capacity and allowed for over 3 hours of unplugged usage. The system no longer reported erratic power levels.

---

## 🧰 Tools Used
- `powercfg /batteryreport`
- Screwdrivers, anti-static wrist strap
- OEM-compatible laptop battery
- Optional: CoconutBattery for macOS diagnostics (if applicable)

---

## 🧠 What I Learned / Explained to the User
- Batteries degrade naturally over time and can cause system instability.
- Windows' `powercfg` tool provides deep insight into battery health.
- Safe handling and matching voltage/specs are critical when replacing internal batteries.
