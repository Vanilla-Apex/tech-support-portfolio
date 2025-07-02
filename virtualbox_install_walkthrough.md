# 🗂️ System Walkthrough: Installing and Configuring VirtualBox on Windows

## 🎯 Purpose

To set up Oracle VirtualBox on a Windows PC for practicing virtual machine installations, OS testing, and lab environments.

---

## 🖥️ System Details

- **Host OS:** Windows 10
- **RAM:** 8GB
- **Storage:** 256GB SSD

---

## 🪜 Step-by-Step Installation

1️⃣ **Download VirtualBox**  
- Went to [https://www.virtualbox.org/](https://www.virtualbox.org/)  
- Downloaded the Windows hosts installer

2️⃣ **Run the Installer**  
- Double-clicked the installer file  
- Followed prompts, kept default settings  
- Allowed network interfaces installation when prompted

3️⃣ **Launch VirtualBox**  
- Verified installation by launching VirtualBox  
- Confirmed version: 7.0.x

4️⃣ **Created First VM**  
- Clicked “New”  
- Named VM: `Ubuntu_Test_VM`  
- Selected Linux → Ubuntu (64-bit)  
- Assigned 2048MB RAM  
- Created a 20GB dynamically allocated virtual hard disk

5️⃣ **Configured VM Settings**  
- Set up the boot order (Optical, Hard Disk)  
- Enabled 2 CPU cores under System → Processor  
- Attached Ubuntu ISO to the optical drive

6️⃣ **Booted VM**  
- Started VM  
- Verified Ubuntu installer launched correctly

---

## ✅ Outcome

- Successfully installed VirtualBox and created a functional Ubuntu VM environment for future labs.
- Ensured VM runs smoothly with network access for updates and package installations.

---

## 💡 Skills Practiced

- Software installation on Windows
- Virtual machine creation and configuration
- Basic understanding of virtualization for lab practice

---

## 📌 Next Steps

Plan to install additional OS environments for testing networking and server configurations.
