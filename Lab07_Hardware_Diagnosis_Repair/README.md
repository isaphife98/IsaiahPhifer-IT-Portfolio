# 🛠️ Lab 07 – Hardware Diagnosis & Repair  
This lab simulates a full hardware troubleshooting and disk replacement workflow, similar to what a Helpdesk or Jr. SysAdmin performs when a server begins showing disk reliability issues.  

Using Windows Server 2019, VirtualBox, built‑in diagnostic tools, and Clonezilla, I diagnosed disk warnings, added replacement hardware, cloned the system disk, and validated a successful migration.

---

# 📂 Lab Structure (Clickable Folders)

### ▶️ **[Step01_Diagnose_Hardware](Step01_Diagnose_Hardware)**
Identify symptoms, analyze NTFS warnings, check SMART data, validate system information, and run file system diagnostics.

### ▶️ **[Step02_Add_Replacement_Disk](Step02_Add_Replacement_Disk)**
Attach a new 120GB virtual disk to simulate hardware replacement and verify detection in Disk Management.

### ▶️ **[Step03_Clone_OS_Using_Clonezilla](Step03_Clone_OS_Using_Clonezilla)**
Clone the OS from the failing disk to the new one using Clonezilla’s disk‑to‑disk mode. Includes warnings, partition table selection, fsck options, and final logs.

### ▶️ **[Step04_Validate_Repair](Step04_Validate_Repair)**
Remove the ISO, boot normally, confirm successful migration, and verify the old failing disk is offline.

---

# 🧩 Step-by-Step Breakdown

---

## 📁 **Step 01 – Diagnose the Hardware Issue**  
**Screenshots stored in:**  
👉 [Step01_Diagnose_Hardware](Step01_Diagnose_Hardware)

### **Actions Performed**
- Reviewed **Event Viewer → System → Disk & NTFS logs**  
- Identified repeated NTFS/UBPM entries suggesting potential disk reliability issues  
- Collected full system hardware info via **msinfo32**  
- Opened **Components → Storage → Disks** for sector and partition validation  
- Ran **CHKDSK** to verify file system integrity  
- Collected **WMIC SMART status**  
- Documented base **Disk Management** layout before adding new hardware  

---

## 📁 **Step 02 – Add Replacement Disk**  
**Screenshots stored in:**  
👉 [Step02_Add_Replacement_Disk](Step02_Add_Replacement_Disk)

### **Actions Performed**
- Added a **120GB VDI** as the new replacement disk  
- Verified Disk 1 appears as **Unallocated**  
- Confirmed Disk 0 remains the primary boot drive  
- Prepared environment for cloning  

---

## 📁 **Step 03 – Clone OS to New Disk Using Clonezilla**  
**Screenshots stored in:**  
👉 [Step03_Clone_OS_Using_Clonezilla](Step03_Clone_OS_Using_Clonezilla)

### **Actions Performed**
- Downloaded and mounted **Clonezilla Live ISO**  
- Booted into disk‑to‑disk cloning mode  
- Chose the correct **source (Disk 0)** and **destination (Disk 1)**  
- Set expert parameters:  
  - `-k0` Keep partition table from source  
  - `-sfsck` Skip filesystem checking  
- Acknowledged overwrite warnings  
- Captured cloning progress and final logs showing success  

---

## 📁 **Step 04 – Validate the Repair**  
**Screenshots stored in:**  
👉 [Step04_Validate_Repair](Step04_Validate_Repair)

### **Actions Performed**
- Removed Clonezilla ISO  
- Booted system normally from new disk  
- Verified Disk 1 is now the **active system disk**  
- Set Disk 0 (old failing disk) **Offline**  
- Confirmed:  
  ✔ System boots correctly  
  ✔ No NTFS warnings  
  ✔ Expanded capacity available (118GB)  

---

# 📈 Final Outcome
✔ Successful hardware diagnosis  
✔ Replacement disk installed  
✔ OS cloned with no data loss  
✔ Old disk safely removed  
✔ Server fully operational on upgraded storage  

---

# 🧠 Reflection
This lab reinforced real‑world IT support skills, including:  
- Reading Event Viewer disk warnings  
- Distinguishing between logical vs. physical problems  
- Using WMIC, CHKDSK, and msinfo32 for diagnostics  
- Cloning drives with Clonezilla  
- Completing a clean hardware replacement workflow  
- Documenting troubleshooting steps professionally  