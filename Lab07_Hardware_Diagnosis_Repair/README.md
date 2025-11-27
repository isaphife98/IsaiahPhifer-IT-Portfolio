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
Lab03_Hardware_Diagnosis/
│
├── README.md
│
├── Step01_Identify_Failure/
│      Step 01 - Event Viewer Disk Warning.png
│      Step 01 - Disk Warning Details.png
│      Step 01 - System Components Overview.png
│      Step 01 - System Information Summary.png
│
├── Step02_Diagnostics/
│      Step 02 - WMIC SMART Status Check.png
│      Step 02 - CHKDSK Scan Results.png
│      Step 02 - Disk Management Initial View.png
│
├── Step03_Add_Replacement_Drive/
│      Step 03 - VirtualBox Storage Before Changes.png
│      Step 03 - Add New Virtual Disk.png
│      Step 03 - New Disk Added to VM.png
│      Step 03 - New Disk Detected in Windows.png
│
└── Step04_Initialize_And_Format/
       Step 04 - New Disk Unallocated Space.png
       Step 04 - Initialize Disk Popup.png
       Step 04 - Disk Set to Online.png
       Step 04 - New Simple Volume Wizard.png
       Step 04 - Assign Drive Letter.png
       Step 04 - Format New Drive.png
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
