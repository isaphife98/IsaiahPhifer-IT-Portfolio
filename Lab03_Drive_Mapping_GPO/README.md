# Lab 03 – Drive Mapping via Group Policy (Item-Level Targeting)
**Active Directory • GPO • File Services • Client Management**

This lab demonstrates how to assign network drive mappings using **Group Policy Preferences** with **Item-Level Targeting (ILT)** so each department receives only the drives assigned to them.

---

## 📁 STEP 01 — Create_Shares  
**Screenshots stored in:**  
[STEP 01 — Create_Shares](STEP%2001%20%E2%80%94%20Create_Shares/)

### Actions Performed:
- Created departmental and public network shares (HR, Helpdesk, IT, Public)  
- Configured share-level permissions  
- Prepared NTFS and directory structure for ILT  

---

## 📁 STEP 02 — Validate NTFS Permissions  
**Screenshots stored in:**  
[STEP 02 — Validate NTFS Permissions](STEP%2002%20%E2%80%94%20Validate%20NTFS%20Permissions/)

### User ↔ Group Mapping:
| User          | Group        | Department |
|---------------|--------------|------------|
| Sarah Jones   | HR           | HR         |
| Brian Lopez   | Helpdesk     | Helpdesk   |
| Michael Reed  | IT Admins    | IT         |

---

## 📁 STEP 03 — Create GPO Drive Mappings  
**Screenshots stored in:**  
[STEP 03 — Create GPO Drive Mappings](STEP%2003%20%E2%80%94%20Create%20GPO%20Drive%20Mappings/)

### GPO Created:
**“Department Drive Mapping GPO”**

Includes mappings for:

- H:\ → HR  
- D:\ → Helpdesk  
- I:\ → IT Admin  
- P:\ → Public  

Configured through:


