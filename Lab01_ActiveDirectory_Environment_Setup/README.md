# Lab 01 – Active Directory Environment Setup & User Management

This lab demonstrates creating a full Windows Server 2019 AD environment, configuring DHCP/DNS, creating users and groups, applying GPOs, and verifying client-side behavior.

---

## 📁 01 — Server Setup
Screenshots show:
- VirtualBox VM creation  
- Attaching Server 2019 ISO  
- Installing Windows Server  
- First login as Administrator  
- Server Manager initial configuration  

---

## 📁 02 — DHCP & DNS Configuration
Configured DHCP Scope Options:
- 003 Router → 10.0.0.10  
- 006 DNS Server → 10.0.0.10  
- 015 DNS Domain Name → adlab.local  

AD DS and DNS roles were installed and verified running.

---

## 📁 03 — Group Policy Objects

### ✔ Drive Mapping GPO  
- Created shared folder on server  
- Configured Drive Mapping in Group Policy Preferences  
- Applied **Item-Level Targeting** based on security groups  
- Verified server shares via Computer Management  

---

## 📁 04 — Client Testing
Validation included:
- Running `gpupdate /force`  
- Checking applied GPOs with RSOP  
- Testing mapped drives for each user  
- Confirming proper access restrictions (deny/allow)  
- Confirming folder permissions work as expected  

Users tested:
- Brian Lopez  
- Sarah Johnson  
- Michael Reed  

Each screenshot shows whether the user has correct access.

---

## 🎯 Final Result
A fully functioning AD environment was built with:
- Windows Server 2019 domain controller  
- DHCP & DNS configuration  
- OU, Group, and User structure  
- Drive Mapping GPO with item-level targeting  
- Client-side verification  

This matches real enterprise helpdesk/sysadmin workflows.
