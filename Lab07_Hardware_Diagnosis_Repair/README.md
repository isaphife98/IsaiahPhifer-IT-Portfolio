# Lab 07 – Hardware Diagnosis & Repair
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

# 🟦 Step-by-Step Process

## 🟦 Step 01 – Identify Hardware Failure
📁 **Screenshots:**  
[Step 01 – Identify Hardware Failure](Step%2001%20%E2%80%93%20Identify%20Hardware%20Failure/)

I examined **Event Viewer → System Logs** and identified repeated disk I/O warnings indicating a failing storage device.

Then I collected system-wide hardware information to understand the full context before replacement.

---

## 🟦 Step 02 – Run Diagnostics
📁 **Screenshots:**  
[Step 02 – Run Diagnostics (SMART, CHKDSK)](Step%2002%20%E2%80%93%20Run%20Diagnostics%20%28SMART,%20CHKDSK%29/)

### ✔ SMART Status  
Command:
```powershell
wmic diskdrive get status
```

### ✔ CHKDSK Scan  
Command:
```powershell
chkdsk /scan
```

### ✔ Disk Management  
Confirmed degraded disk state visually.

---

## 🟦 Step 03 – Simulate Faulted Drive & Add New Virtual Disk
📁 **Screenshots:**  
[Step 03 – Simulate Faulted Drive & Add New Virtual Disk](Step%2003%20%E2%80%93%20Simulate%20Faulted%20Drive%20%26%20Add%20New%20Virtual%20Disk/)

In **VirtualBox → Settings → Storage**, I added a new virtual hard disk to simulate replacing the failing physical drive.

On reboot, Windows automatically detected the new disk.

---

## 🟦 Step 04 – Initialize and Format Replacement Disk
📁 **Screenshots:**  
[Step 04 – Initialize and Format Replacement Disk](Step%2004%20%E2%80%93%20Initialize%20and%20Format%20Replacement%20Disk/)

Using **Disk Management**, I completed the replacement:

- Brought disk online  
- Initialized disk (MBR or GPT)  
- Created a new simple volume  
- Assigned drive letter  
- Formatted using NTFS  
- Verified healthy status  

---

# 📘 Summary / Takeaways

This lab demonstrates essential IT technician and Helpdesk skills:

- Reading & interpreting hardware failure logs  
- Running SMART & CHKDSK diagnostics  
- Managing storage and partitions in Windows  
- Simulating real hardware replacement in VirtualBox  
- Understanding initialization, partitioning, and formatting  
- Restoring full disk functionality after hardware failure  
