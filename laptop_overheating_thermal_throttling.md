# 🛠️ Diagnosing and Fixing Laptop Overheating & Thermal Throttling

## 📍 Summary
A Windows 10 laptop was experiencing sudden performance drops, fan spikes, and system lag during light tasks. After investigation, I determined the root cause was **thermal throttling** due to dust buildup and deteriorated thermal paste on the CPU.  
This case study covers diagnostics, disassembly, cleaning, thermal repaste, and final verification.

---

## 🔎 Symptoms
- Laptop would suddenly slow down during normal use  
- CPU frequency repeatedly dropped to ~0.40 GHz  
- Fans ran at maximum RPM frequently  
- The chassis felt unusually hot near the exhaust and keyboard  
- Games and video playback stuttered  
- Occasional forced shutdowns after extended use  

---

## 🧪 Diagnostics Performed

### **1. Verified Throttling with Task Manager**
- Observed CPU usage spiking to 100% with low clock speeds  
- “Power throttling” and “Thermal throttling” indicators appeared intermittently  

### **2. Checked Temperatures Using HWMonitor**
- Idle CPU temps: **55–60°C** (too high)  
- Load temps: **95–100°C**, triggering throttling  
- GPU temps also elevated  

### **3. Physical Inspection**
After shutting down and removing the back cover:
- Dust clogging the fan and heatsink fins  
- Dry, cracked thermal paste on CPU and GPU  
- Fan blades coated with debris  

### **4. Ruled Out Software Causes**
- No malware  
- Windows updates applied  
- Power settings at High Performance  
- BIOS up to date  

Hardware was confirmed as the primary issue.

---

## 🔧 Resolution

### **1. Full Internal Cleaning**
- Removed back panel using appropriate screwdriver bit  
- Carefully cleaned fan housing and heatsink with compressed air  
- Removed residual dust from vents and chassis using a soft anti-static brush  

### **2. Thermal Paste Replacement**
- Cleaned old paste using isopropyl alcohol (99%) and microfiber swabs  
- Applied a high-quality thermal compound (Arctic MX-6) using a pea-sized method  
- Reassembled heatsink with even torque on all screws  

### **3. Fan and Vent Realignment**
- Ensured fans were connected securely  
- Confirmed no cable obstruction  

### **4. Post-Repair Temperature Test**
Using Cinebench R23 and HWMonitor:
- Idle CPU temps: **38–42°C**  
- Load temps: **72–78°C**  
- Zero thermal throttling during extended load  
- System remained stable and quiet  

---

## 🧩 Root Cause
- Dust accumulation blocked airflow  
- Old thermal paste failed to conduct heat properly  
- Result: **thermal throttling**, lower CPU frequency, and system instability  

---

## 📘 Skills Demonstrated
- Hardware disassembly and safe handling  
- Laptop cooling system maintenance  
- Thermal paste application and system reassembly  
- Use of diagnostics tools (HWMonitor, Cinebench, Task Manager)  
- Clear communication with end user about preventative maintenance  

---

## 🧰 Tools & Materials Used
- Compressed air  
- Isopropyl alcohol (99%)  
- Anti-static brush  
- Arctic MX-6 thermal paste  
- Precision screwdriver set  
- HWMonitor  
- Cinebench R23  

---

## 🧩 Preventative Measures
To avoid future overheating:
- Clean vents every 2–3 months  
- Avoid placing laptop on fabric surfaces  
- Periodically check temps with HWMonitor  
- Consider using a cooling pad for long workloads  
- Schedule thermal paste replacement every 18–24 months  

---

## ✅ Final Outcome
After cleaning and repasting, the laptop operated at safe temperatures under load with no throttling. The user reported a dramatic improvement in performance, fan noise reduction, and overall system stability.

