# 🛠️ Application Failing Due to Disk Space Exhaustion

---

## 🔧 Summary

A user reported that an application was failing to launch and save files, despite previously working without issues. The system displayed intermittent errors during normal operation.

This case study covers diagnosing application failures caused by insufficient disk space and restoring functionality by identifying and resolving storage constraints.

---

## 🔍 Symptoms

- Application failing to launch or crashing  
- Errors when attempting to save files  
- System performance degraded  
- Intermittent error messages without clear cause  
- Issue developed gradually over time  

---

## 🔎 Diagnostics Performed

### 1. Verified application behavior

- Attempted to launch the application  
- Observed failure during startup  
- Confirmed errors occurred when saving files  

### 2. Checked system performance

- Observed general system slowdown  
- Verified CPU and memory usage were within normal ranges  
- Identified no immediate resource bottlenecks  

### 3. Checked disk space

- Opened file explorer to review storage usage  
- Identified system drive was nearly full  
- Confirmed available disk space was critically low  

### 4. Investigated disk usage

- Reviewed large files and folders  
- Identified temporary files and unused data consuming space  
- Confirmed lack of available space was impacting application behavior  

### 5. Freed disk space

- Removed temporary files and unnecessary data  
- Cleared system cache where applicable  
- Ensured sufficient free space was restored  

### 6. Retested application

- Relaunched the application  
- Verified successful startup  
- Confirmed normal file-saving functionality  

---

## ✅ Result

After freeing disk space, the application functioned normally. Errors were resolved, and system performance improved.

---

## 🧰 Tools Used

- File Explorer  
- Disk usage inspection  
- System cleanup processes  

---

## 🧠 What I Learned / Explained to the User

- Low disk space can cause unexpected application failures  
- Storage issues may not present clear error messages  
- Regular cleanup helps prevent system instability  
- Verifying system resources is essential when diagnosing application issues  
