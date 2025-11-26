# Lab 05 – NTFS & Share Permissions Configuration
**Windows Server • File Security • NTFS ACLs • Helpdesk Troubleshooting**

This lab demonstrates configuring secure, department-based file access using **NTFS permissions**, one of the most essential skills for Helpdesk and System Administrators.  
You test permissions with multiple users and validate both access and denial scenarios.

---

## 📌 Objectives

- Create department folders: **HR, IT, Helpdesk**  
- Configure NTFS permissions (Allow / Modify / Read)  
- Assign access using Active Directory security groups  
- Simulate user access tests  
- Confirm cross-department restrictions work correctly  

---

## 🟦 Step 01 – Create Department Folders

Created the following folders on a shared volume/server:

- **HR**  
- **IT**  
- **Helpdesk**

Each folder received base NTFS permissions before group assignments.

📁 **Screenshots:**  
[Step 01 — Create Department Folders](Step 01 — Create Department Folders/)

---

## 🟦 Step 02 – Configure NTFS Permissions

Assigned access based on AD security groups:

| Folder   | Who Should Have Access | Permission |
|----------|------------------------|------------|
| HR       | HR Group Only          | Modify     |
| IT       | IT Admins              | Modify     |
| Helpdesk | Helpdesk Group         | Modify     |

Configuration steps included:

- Using the **Security** tab  
- Disabling inheritance  
- Cleaning existing permissions  
- Adding proper AD security groups  
- Confirming user-level permissions  

📁 **Screenshots:**  
[Step 02 — Configure NTFS Permissions](Step 02 — Configure NTFS Permissions/)

---

## 🟦 Step 03 – Test Access

Logged in as:

- **Sarah Jones (HR)**  
- **Brian Lopez (Helpdesk)**  
- **Michael Reed (IT Admin)**  

### ✔ Expected Correct Access:

- HR → Access to **HR folder**  
- IT → Access to **IT folder**  
- Helpdesk → Access to **Helpdesk folder**  

### ❌ Expected Correct Denials:

- HR cannot access **IT** or **Helpdesk**  
- Helpdesk cannot access **HR**  
- IT Admin can access **all folders** (elevated rights)

📁 **Screenshots:**  
[Step 03 — Test Access Restrictions (Positive & Negative Tests)](Step 03 — Test Access Restrictions (Positive & Negative Tests)/)

---

## 📘 Summary

This lab demonstrates:

- Applying NTFS ACLs properly  
- Assigning permissions using AD groups  
- Validating effective permissions with real user logins  
- Troubleshooting “Access Denied” issues  
- Implementing **least privilege security principles**  

A foundational enterprise skill required for:

- Helpdesk  
- Desktop Support  
- Junior SysAdmin  
- Windows Administration roles  

