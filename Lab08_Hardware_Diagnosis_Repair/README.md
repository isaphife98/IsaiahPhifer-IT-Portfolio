# Lab 03 – Hardware Diagnosis & Repair
**IT Support • Hardware Troubleshooting • Disk Management • Virtualization**

This lab simulates a real-world hardware failure scenario, including diagnosing a failing disk (SMART/CHKDSK), verifying warning events in Event Viewer, and performing a clean replacement using a new virtual disk inside VirtualBox.

---

## 📌 Objectives

- Detect hardware issues using **Event Viewer**  
- Run diagnostic commands (SMART, CHKDSK)  
- Examine system information for hardware context  
- Add a replacement hard drive in **VirtualBox**  
- Initialize, partition, and format the new disk  
- Validate successful disk replacement  

---

## 🛠️ Technologies Used

- Windows 10 / Windows Server  
- VirtualBox  
- Event Viewer  
- Disk Management  
- WMIC SMART  
- CHKDSK  

---

## 📁 Folder Structure

```

```

---

# 🟦 Step-by-Step Process

## 🟦 Step 01 – Identify Disk Failure

I examined **Event Viewer → System Logs** and identified repeated disk I/O warnings indicating a failing storage device.

Then I collected system-wide hardware information to understand the full context before replacement.

📁 **Screenshots:**  
`Step01_Identify_Failure/`

---

## 🟦 Step 02 – Run Diagnostics

### ✔ SMART Status
Command:
```
wmic diskdrive get status
```
Result: SMART status showed warnings.

### ✔ CHKDSK Scan
Command:
```
chkdsk /scan
```
Result: File system issues were detected.

### ✔ Disk Management
Confirmed degraded disk state visually.

📁 **Screenshots:**  
`Step02_Diagnostics/`

---

## 🟦 Step 03 – Add Replacement Virtual Disk

In **VirtualBox → Settings → Storage**, I added a new virtual hard disk to simulate replacing the failing physical drive.

On reboot, Windows automatically detected the new disk.

📁 **Screenshots:**  
`Step03_Add_Replacement_Drive/`

---

## 🟦 Step 04 – Initialize & Format the New Disk

Using **Disk Management**, I completed the replacement:

- Brought disk online  
- Initialized disk (MBR or GPT)  
- Created a new simple volume  
- Assigned drive letter  
- Formatted using NTFS  
- Verified healthy status  

📁 **Screenshots:**  
`Step04_Initialize_And_Format/`

---

# 📘 Summary / Takeaways

This lab demonstrates essential IT technician and Helpdesk skills:

- Reading & interpreting hardware failure logs  
- Running SMART & CHKDSK diagnostics  
- Managing storage and partitions in Windows  
- Simulating real hardware replacement in VirtualBox  
- Understanding initialization, partitioning, and formatting  
- Restoring full disk functionality after hardware failure  

A realistic simulation of tasks handled by **Helpdesk**, **Desktop Support**, and **Junior SysAdmin** roles.

---

# 🚀 Lab Completed
This lab is finished and ready to upload to your GitHub IT Support portfolio.

