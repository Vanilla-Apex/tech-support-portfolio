# 🛠️ Diagnosing High CPU Usage Causing System Slowdown

---

## 🔧 Summary

A user reported that their computer had become extremely slow during normal use. Applications were taking several seconds to respond and system performance degraded significantly when multiple programs were open.

This case study covers diagnosing excessive CPU utilization by identifying resource-heavy processes and resolving the issue through process management and startup optimization.

---

## 🔍 Symptoms

- System responding slowly during normal use
- Applications taking several seconds to open
- Fans running continuously at high speed
- Performance degradation when multiple applications were open
- Taskbar and window interactions lagging

---

## 🔎 Diagnostics Performed

### 1. Verified system performance symptoms

- Observed slow response when opening applications
- Confirmed system slowdown during multitasking
- Verified that disk activity and memory usage were within normal ranges

### 2. Checked CPU utilization

- Opened **Task Manager**
- Observed CPU usage consistently above 90%
- Identified a background process consuming the majority of CPU resources

### 3. Investigated the process

- Checked the process name and associated application
- Determined the process was related to a recently installed application
- Confirmed the process remained active even when the application was not in use

### 4. Terminated the process and monitored system behavior

- Ended the high-usage process in Task Manager
- CPU utilization immediately returned to normal levels
- System responsiveness improved

### 5. Reviewed startup programs

- Opened the **Startup** tab in Task Manager
- Identified the same application configured to launch automatically
- Disabled the startup entry to prevent recurrence

---

## ✅ Result

After terminating the resource-intensive process and disabling the unnecessary startup program, CPU usage returned to normal levels and system performance was restored.

---

## 🧰 Tools Used

- Windows Task Manager  
- Startup application management  
- System performance monitoring  

---

## 🧠 What I Learned / Explained to the User

- Excessive CPU usage is often caused by background applications rather than hardware failure
- Task Manager provides a quick way to identify resource-intensive processes
- Disabling unnecessary startup programs can prevent recurring performance issues
- Monitoring system resources helps isolate the root cause of performance problems
