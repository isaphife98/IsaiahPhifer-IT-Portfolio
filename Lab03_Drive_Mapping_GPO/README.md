# Lab 03 – Drive Mapping via Group Policy (Item-Level Targeting)
**Active Directory • GPO • File Services • Client Management**

This lab demonstrates how to assign network drive mappings using **Group Policy Preferences** with **Item-Level Targeting (ILT)** so each department only receives its assigned network share.

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

📁 **Screenshots:**  
👉 **[STEP 01 — Create_Shares](./STEP%2001%20%E2%80%94%20Create_Shares/)**

---

## 🟦 Step 02 – Validate NTFS & Group Membership

Mapped security groups:

| User          | Group        | Department |
|---------------|--------------|------------|
| Sarah Jones   | HR           | HR         |
| Brian Lopez   | Helpdesk     | Helpdesk   |
| Michael Reed  | IT Admins    | IT         |

📁 **Screenshots:**  
👉 **[STEP 02 — Validate NTFS Permissions](./STEP%2002%20%E2%80%94%20Validate%20NTFS%20Permissions/)**

---

## 🟦 Step 03 – Configure Drive Mapping GPO

Created GPO:  
**“Department Drive Mapping GPO”**

Included mappings:

- HR Drive → HR group  
- Helpdesk Drive → Helpdesk group  
- IT Drive → IT Admins  
- Public Drive → All authenticated users  

📁 **Screenshots:**  
👉 **[STEP 03 — Create GPO Drive Mappings](./STEP%2003%20%E2%80%94%20Create%20GPO%20Drive%20Mappings/)**

---

## 🟦 Step 04 – Client Testing

Validated with:

- File Explorer  
- gpupdate /force  
- gpresult /r  
- NTFS permission enforcement  

📁 **Screenshots:**  
👉 **[STEP 04 — Client Testing](./STEP%2004%20%E2%80%94%20Client%20Testing/)**

---

## 📘 Summary

This lab demonstrates:

- GPO Preferences for drive mapping  
- Item-Level Targeting  
- NTFS + GPO integration  
- Real-world troubleshooting  
- Enterprise-grade Windows support workflow  
