# 🛠️ Case Study: Linux Disk Full Despite Available Space Due to Inode Exhaustion

---

## 🔧 Summary

A user reported that a Linux system was unable to create new files or install updates, despite showing available disk space. Standard cleanup steps did not resolve the issue, and error messages continued to indicate that the disk was full.

This case study covers diagnosing disk space issues caused by inode exhaustion and restoring normal system operation by identifying and removing excessive small files.

---

## 🔍 Symptoms

- System reported “No space left on device” errors  
- File creation and package updates failed  
- Disk usage appeared normal when checked with standard tools  
- Issue persisted after clearing large files  
- System functionality was partially degraded  

---

## 🧪 Diagnostics Performed

### 1. Verified Disk Usage
- Checked disk space using `df -h`  
- Confirmed that sufficient disk space was available  
- Result: Disk capacity did not explain the issue  

### 2. Investigated Inode Usage
- Checked inode utilization using `df -i`  
- Observed inode usage at or near 100% on the affected filesystem  
- Identified inode exhaustion as the root cause  

### 3. Located High Inode Consumption
- Searched for directories containing large numbers of small files  
- Identified log and cache directories with excessive file counts  
- Confirmed these files were no longer required  

### 4. Cleaned Up Excess Files
- Safely removed unnecessary log and temporary files  
- Rechecked inode usage after cleanup  
- Verified inode availability returned to normal levels  

---

## ✅ Resolution

Removing excessive small files freed up inodes on the filesystem. Once inode usage returned to acceptable levels, the system was able to create files, install updates, and operate normally again.

---

## 🧰 Tools Used

- Linux shell utilities (`df -h`, `df -i`, `du`)  
- File system inspection commands  
- Log and cache directory analysis  

---

## 🧠 What I Learned / Explained to the User

- Disk space and inode availability are separate resources on Linux systems  
- A filesystem can report free space while still being unusable due to inode exhaustion  
- Large numbers of small files can silently consume all available inodes  
- Regular log and cache maintenance helps prevent this class of issue  
