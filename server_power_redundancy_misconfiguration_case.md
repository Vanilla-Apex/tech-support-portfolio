# 🛠️ Case Study: Server Fails to Power On Due to Incorrect Power Redundancy Configuration (Simulated Data Center Scenario)

---

## 🔧 Summary

This case study documents a simulated data center scenario in which a newly installed server failed to power on due to incorrect power redundancy configuration.

The objective of this exercise was to identify power-related issues by validating dual power supply connections and ensuring proper A/B feed separation before escalating or replacing hardware.

---

## 🔍 Scenario

A server installed in a rack does not power on when the power button is pressed. No hardware fault indicators are present, and the installation was recently completed.

This scenario simulates a common data center issue where power redundancy is misconfigured rather than hardware being defective.

---

## 🧪 Diagnostics / Validation Performed

### 1. Verified Physical Power Connections
- Confirmed both power supplies were present  
- Checked that power cables were firmly seated  

### 2. Validated Power Source Separation
- Identified that both power supplies were connected to the same power source  
- Confirmed lack of A/B feed separation  

### 3. Corrected Power Configuration
- Reconnected one power supply to an alternate power source  
- Ensured cables were properly routed and strain-free  

### 4. Retested Power-On Behavior
- Powered on the server after correcting redundancy  
- Verified normal startup behavior  

---

## ✅ Outcome

Correcting the power redundancy configuration restored normal power-on behavior. The server powered on successfully without requiring hardware replacement.

---

## 🧰 Tools Used

- Visual inspection  
- Power redundancy checklist  
- Data center power best-practice guidelines  

---

## 🧠 What I Learned / Explained

- Dual power supplies do not provide redundancy if connected to the same source  
- Power issues should be validated before assuming hardware failure  
- Correct power configuration reduces unnecessary troubleshooting and downtime  
