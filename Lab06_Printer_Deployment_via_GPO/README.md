# Lab 06 🚀 Drive Mapping via Group Policy (Item-Level Targeting)
**Active Directory • GPO • File Services • Client Management**

This lab demonstrates how to deploy network drive mappings using **Group Policy Preferences** with **Item-Level Targeting (ILT)** so each department receives only the drives assigned to them.

This reflects a daily real-world task for Helpdesk & SysAdmin teams.

---

## 📁 STEP 01 — Create_Shares  
**Screenshots stored in:** `STEP 01 — Create_Shares`

### Actions Performed:
Created departmental and public network shares:

- HR  
- Helpdesk  
- IT  
- Public  

Initial NTFS + share structure prepared for ILT.

---

## 📁 STEP 02 — Validate NTFS Permissions  
**Screenshots stored in:** `STEP 02 — Validate NTFS Permissions`

### User ↔ Group Mapping:

| User          | Group        | Department |
|---------------|--------------|------------|
| Sarah Jones   | HR           | HR         |
| Brian Lopez   | Helpdesk     | Helpdesk   |
| Michael Reed  | IT Admins    | IT         |

Correct NTFS permissions ensure that ILT can enforce access correctly.

---

## 📁 STEP 03 — Create GPO Drive Mappings  
**Screenshots stored in:** `STEP 03 — Create GPO Drive Mappings`

### GPO: **“Department Drive Mapping GPO”**

Configured drive mappings:

- **H:\ → HR** (HR Group Only)  
- **D:\ → Helpdesk** (Helpdesk Group Only)  
- **I:\ → IT Admin** (IT Admins Only)  
- **P:\ → Public** (Authenticated Users)

Configured via:

```
User Configuration  
   → Preferences  
       → Windows Settings  
           → Drive Maps  
```

Each drive mapping included:

- Assigned drive letter  
- UNC path  
- Action: Replace  
- Item-Level Targeting → Security Group Filter  

---

## 📁 STEP 04 — Client Testing  
**Screenshots stored in:** `STEP 04 — Client Testing`

### Expected Results:

#### ✔ Sarah (HR)  
- H:\ HR  
- P:\ Public  
❌ No Helpdesk  
❌ No IT  

#### ✔ Brian (Helpdesk)  
- D:\ Helpdesk  
- P:\ Public  
❌ No HR  
❌ No IT  

#### ✔ Michael (IT Admin)  
- I:\ IT Admin  
- P:\ Public  
✔ May see additional shares depending on broader permissions  

Validation performed using:

- gpupdate /force  
- gpresult /r  
- File Explorer access tests  
- Permission enforcement checks  

---

## 🧠 Summary

This lab demonstrates:

- Group Policy Preferences for drive mapping  
- Item-Level Targeting using AD security groups  
- NTFS + GPO integration  
- Correct departmental share deployment  
- Real-world troubleshooting and verification  
- Enterprise-grade Windows administration workflow  
