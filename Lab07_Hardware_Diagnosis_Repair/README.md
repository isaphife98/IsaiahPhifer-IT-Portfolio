# 🛠️ Lab 07 Hardware Diagnosis & Disk Replacement Lab
Windows Server 2019 • VirtualBox • Clonezilla • Disk Management • System Diagnostics

This lab demonstrates a full end-to-end hardware troubleshooting and disk replacement workflow.
Using Windows Server 2019 and Clonezilla, I diagnosed disk reliability warnings, added replacement hardware, cloned the OS to a new disk, and validated the server’s recovery—mirroring a real-world Helpdesk / SysAdmin repair scenario.

---

# 🧩 Lab Environment
**Host:** Windows 10 Pro (VirtualBox)  
**Server OS:** Windows Server 2019 Standard Evaluation  
**vCPU:** 2  
**RAM:** 4 GB  
**Primary Disk (Disk 0):** 60GB VHD (failing)  
**Replacement Disk (Disk 1):** 120GB VHD  
**Cloning Tool:** Clonezilla Live ISO  
**Diagnostics:** CHKDSK • WMIC SMART • Event Viewer • msinfo32  

---

# 🧩 Skills Demonstrated
- Diagnosing hardware reliability issues  
- Reviewing NTFS, Disk, and UBPM warnings  
- Verifying disk health (SMART, CHKDSK, msinfo32)  
- Adding and configuring replacement storage hardware  
- Using Clonezilla for disk-to-disk OS cloning  
- Validating disk migration and boot integrity  
- Performing real-world Helpdesk troubleshooting workflow  
- Clean documentation and IT ticket–style reporting  

---

# 📁 Step 01 — Diagnose the Hardware Issue
Screenshots stored in:  
➡️ **[Step01_Diagnose_Hardware](Step01_Diagnose_Hardware)**

### Actions Performed
- Reviewed **Event Viewer → System** for NTFS and disk warnings  
- Verified disk model, size, and sector configuration via **msinfo32**  
- Inspected disk-level details using **Components → Storage → Disks**  
- Ran **CHKDSK** to validate file system integrity  
- Checked SMART status:
  ```bash
  wmic diskdrive get status
  ```
- Documented original state in **Disk Management** before adding replacement disk  

---

# 📁 Step 02 — Add Replacement Disk
Screenshots stored in:  
➡️ **[Step02_Add_Replacement_Disk](Step02_Add_Replacement_Disk)**

### Actions Performed
- Created a new **120GB VDI** as the replacement hard disk  
- Attached the drive to the virtual machine as **Disk 1**  
- Verified Disk 1 appeared as **Unallocated** in Disk Management  
- Confirmed Disk 0 remained online and bootable prior to cloning  

---

# 📁 Step 03 — Clone OS to New Disk Using Clonezilla
Screenshots stored in:  
➡️ **[Step03_Clone_OS_Using_Clonezilla](Step03_Clone_OS_Using_Clonezilla)**

### Actions Performed
- Mounted **Clonezilla Live** ISO and booted into recovery mode  
- Selected: **device-device → disk_to_local_disk**  
- Chose **Disk 0 (source)** → **Disk 1 (destination)**  
- Applied advanced options:
  - `-k0` keep source partition table  
  - `-sfsck` skip filesystem checking  
- Acknowledged all overwrite warnings  
- Captured Clonezilla progress and success confirmation  
- Shut down VM to begin using new hardware  

---

# 📁 Step 04 — Validate the Repair
Screenshots stored in:  
➡️ **[Step04_Validate_Repair](Step04_Validate_Repair)**

### Actions Performed
- Removed Clonezilla ISO and performed a standard boot  
- Verified Disk 1 now contains the cloned system partitions  
- Confirmed Disk 1 marked **Healthy (Boot, Active, Primary)**  
- Set Disk 0 (failing disk) **Offline**  
- Validated clean boot, stability, and increased storage capacity  

---

# ✅ Summary
This lab demonstrates the complete workflow for diagnosing and repairing a failing disk in a Windows Server environment:

- Identified early disk failure symptoms  
- Verified system and disk health using built-in tools  
- Installed and validated replacement hardware  
- Performed an OS clone using Clonezilla  
- Confirmed proper booting and disk structure on new hardware  
- Retired the faulty disk safely  

This mirrors real-world responsibilities of **Helpdesk**, **Desktop Support**, and **SysAdmin** roles.

