# 🛠️ Case Study: Network Interface Link Down After Rack Installation (Simulated Data Center Scenario)

---

## 🔧 Summary

This case study documents a simulated scenario in which a server showed no network connectivity after rack installation due to cabling and port-level issues.

The focus of this exercise was to validate physical network connections and isolate link-layer problems before escalating to network teams.

---

## 🔍 Scenario

A newly installed server powers on successfully but shows no network connectivity. Link lights are inactive, and the server cannot be reached over the network.

This scenario simulates a common post-installation networking issue in data center environments.

---

## 🧪 Diagnostics / Validation Performed

### 1. Verified Physical Network Connections
- Confirmed network cables were securely connected  
- Checked NIC ports for activity indicators  

### 2. Inspected Switch Port Assignment
- Verified cables were connected to the correct switch ports  
- Confirmed ports were enabled and not administratively disabled  

### 3. Validated Cable Labeling and Routing
- Checked cable labels for accuracy  
- Ensured cables were routed cleanly and not under tension  

### 4. Retested Network Link Status
- Observed NIC LEDs after reseating cables  
- Confirmed link status was restored  

---

## ✅ Outcome

Correcting the cabling and port assignment restored network connectivity. The server established a network link without requiring configuration changes.

---

## 🧰 Tools Used

- Visual inspection  
- Network cable labeling standards  
- NIC link indicators  

---

## 🧠 What I Learned / Explained

- Physical cabling issues are common after rack installation  
- Link-layer validation should precede software troubleshooting  
- Clear cable labeling simplifies rapid issue resolution  
