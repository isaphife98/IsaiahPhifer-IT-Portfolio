# Lab 03 Drive Mapping via Group Policy (Item-Level Targeting)
**Active Directory • GPO • File Services • Client Management**

This lab demonstrates how to assign network drive mappings using **Group Policy Preferences** with **Item-Level Targeting (ILT)** so each department only receives its assigned network share.

This is a real configuration performed daily by Helpdesk & SysAdmin teams.

---

## 📌 Objectives

- Create Public + Department shared folders  
- Ensure NTFS permissions match AD security groups  
- Build Drive Mapping GPO using ILT  
- Test mappings using HR, Helpdesk, and IT user accounts  
- Confirm users only see the drives assigned to their department  

---

## 🟦 Step 01 – Create Shared Folders

Created:

- HR
- Helpdesk
- IT
- Public

Set initial share structure.

📁 **Screenshots:**  
`Step01_Create_Shares/`

---

## 🟦 Step 02 – Validate NTFS & Group Membership

Mapped security groups:

| User          | Group        | Department |
|---------------|--------------|------------|
| Sarah Jones   | HR           | HR         |
| Brian Lopez   | Helpdesk     | Helpdesk   |
| Michael Reed  | IT Admins    | IT         |

Correct NTFS permissions ensure ILT works properly.

📁 **Screenshots:**  
`Step02_Validate_NTFS_and_Groups/`

---

## 🟦 Step 03 – Configure Drive Mapping GPO

Created GPO:

**“Department Drive Mapping GPO”**

Included mappings:

✔ HR Drive – only if user ∈ HR  
✔ Helpdesk Drive – only if user ∈ Helpdesk  
✔ IT Drive – only if user ∈ IT Admins  
✔ Public Drive – for all Authenticated Users  

Used these settings:

```
User Configuration
   → Preferences
       → Windows Settings
           → Drive Maps
```

Each drive mapping configured with:

- Assigned drive letter  
- UNC path  
- Action: Replace  
- Item-Level Targeting → Security Group Filter

📁 **Screenshots:**  
`Step03_Create_Drive_Mapping_GPO/`

---

## 🟦 Step 04 – Client Testing (Sarah, Brian, Michael)

### Sarah (HR) should see:
- H:\ HR  
- P:\ Public  
❌ No IT  
❌ No Helpdesk  

### Brian (Helpdesk) should see:
- D:\ Helpdesk  
- P:\ Public  
❌ No HR  
❌ No IT  

### Michael (IT Admin) should see:
- I:\ IT Admin  
- P:\ Public  
✔ May see additional shares depending on full NTFS rights  

Validated with:

- File Explorer  
- gpupdate /force  
- Incorrect access attempts  
- NTFS permission enforcement  

📁 **Screenshots:**  
`Step04_Client_Testing/`

---

## 📘 Summary

This lab demonstrates:

- GPO Preferences for drive mapping  
- Item-Level Targeting using security groups  
- Best practices for user-based drive deployment  
- Correct integration of NTFS + GPO  
- Real-world troubleshooting scenarios  
- Enterprise-grade Windows support workflow  
