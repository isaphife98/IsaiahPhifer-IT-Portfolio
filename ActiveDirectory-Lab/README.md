# Active Directory Lab

This project demonstrates how I stood up and administered a Windows Server 2019 Active Directory Domain Services (AD DS) environment. I built a domain, organized users and computers, and verified domain logons from a Windows 10 client.

---

## 🛠 Tools & Technologies

- Windows Server 2019
- Active Directory Domain Services (AD DS)
- DNS
- Windows 10 (CLIENT01)
- VirtualBox

---

## ✅ What I Completed

- Installed Windows Server 2019 and configured basic networking
- Promoted the server to a Domain Controller and created the domain **adlab.local**
- Created a clean OU structure for:
  - Departments
  - Users
  - Workstations
- Created named domain users and assigned them to departmental security groups (HR, Helpdesk, IT)
- Joined a Windows 10 workstation (**CLIENT01**) to the domain
- Logged in as multiple users from CLIENT01 to verify:
  - Domain authentication
  - Group membership
  - That user logons were being processed by the domain

---

## 📸 Screenshots

Store files in: `ActiveDirectory-Lab/screenshots/`

Suggested screenshots:
- ADUC OU structure
- User accounts and security groups
- CLIENT01 joined to the domain
- Successful domain logon

---

## 🧠 Skills Demonstrated

- Enterprise identity management (AD DS)
- Domain controller deployment
- DNS dependency for Active Directory
- Organizational Unit (OU) and group design
- Domain workstation join and verification

---

## 📁 Folder Layout

```text
ActiveDirectory-Lab/
├── screenshots/
└── README.md
