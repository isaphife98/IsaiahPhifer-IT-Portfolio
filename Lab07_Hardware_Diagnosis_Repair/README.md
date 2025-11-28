# 🛠️ Hardware Diagnosis & Disk Replacement Lab
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
- Identifying disk warnings through **Event Viewer** (NTFS, Disk, UBPM)  
- Checking physical health using **SMART**, **CHKDSK**, and **msinfo32**  
- Adding and configuring replacement virtual hardware  
- Performing a full **disk-to-disk OS clone**  
- Using Clonezilla expert mode flags and understanding safe-clone behavior  
- Validating boot configuration and partition structure  
- Documenting real-world troubleshooting and repair workflow  

---

# 📁 Step 01 — Diagnose the Hardware Issue
Screenshots stored in:  
➡️ **Step01_Diagnose_Hardware**

### Actions Performed
- Reviewed **Event Viewer → System** and filtered Disk + NTFS logs  
- Identified repeated NTFS warnings indicating reliability degradation  
- Used **msinfo32** to review full system and disk details  
- Captured **sector count**, disk size, and partition layout  
- Ran **CHKDSK C:** to validate file system integrity  
- Verified disk’s SMART status using:
  ```bash
  wmic diskdrive get status
  ```  
- Documented original **Disk Management** layout before replacement disk was added  

---

# 📁 Step 02 — Add Replacement Disk
Screenshots stored in:  
➡️ **Step02_Add_Replacement_Disk**

### Actions Performed
- Created a new **120GB VDI** in VirtualBox  
- Attached it to the server VM as **Disk 1**  
- Confirmed the new disk appeared as **Unallocated** in Disk Management  
- Ensured the failing disk (Disk 0) remained online before cloning  
- Prepared environment for Clonezilla migration  

---

# 📁 Step 03 — Clone OS to New Disk Using Clonezilla
Screenshots stored in:  
➡️ **Step03_Clone_OS_Using_Clonezilla**

### Actions Performed
- Downloaded and mounted **Clonezilla Live** ISO  
- Booted into Clonezilla and selected:  
  **device-device → disk_to_local_disk**  
- Selected **Disk 0 (source)** → **Disk 1 (destination)**  
- Applied expert options:  
  - `-k0` Keep original partition table  
  - `-sfsck` Skip filesystem check  
- Accepted overwrite warnings for Disk 1  
- Captured cloning progress, logs, and final "completed successfully" output  
- Shutdown Clonezilla to prepare for normal boot  

---

# 📁 Step 04 — Validate the Repair
Screenshots stored in:  
➡️ **Step04_Validate_Repair**

### Actions Performed
- Removed Clonezilla ISO  
- Booted normally from the **new 120GB disk**  
- Verified partitions (System Reserved + C:) cloned successfully  
- Confirmed Disk 1 marked **Healthy (Active, Boot, Primary Partition)**  
- Set Disk 0 (old disk) **Offline** to simulate hardware removal  
- Confirmed system stability, no NTFS warnings, and new storage capacity available  

---

# ✅ Summary
This lab demonstrates a realistic, enterprise-style hardware replacement workflow:

- Identified early disk failure symptoms using NTFS logs  
- Verified disk health with SMART, CHKDSK, and diagnostic tools  
- Added and configured new replacement hardware  
- Performed a complete OS migration using Clonezilla  
- Validated server boot integrity on the new disk  
- Safely retired the failing drive  

This mirrors real-world responsibilities in **Helpdesk**, **Desktop Support**, and **Junior System Administrator** roles, showing proficiency in diagnostics, imaging, and hardware lifecycle management.
