# 🖥️ Lab 01 – Active Directory Environment Setup & User Management

This lab demonstrates building a full Windows Server 2019 Active Directory environment, configuring DHCP/DNS, creating users and groups, applying GPOs, and verifying all functionality on the client machine.

---

## 📁 01-ServerSetup  
**Screenshots stored in:** `01-ServerSetup`

### Actions Performed:
- Created a new VirtualBox VM  
- Attached the Windows Server 2019 ISO  
- Installed Windows Server and completed initial setup  
- Logged in as **Administrator**  
- Performed initial Server Manager configuration (computer name, IP settings, etc.)

---

## 📁 02-DHCP_DNS  
**Screenshots stored in:** `02-DHCP_DNS`

### Actions Performed:
- Installed **Active Directory Domain Services**, **DNS**, and **DHCP**  
- Promoted the server to a domain controller for **adlab.local**  
- Created a DHCP Scope with:  
  - **003 Router** → 10.0.0.10  
  - **006 DNS Server** → 10.0.0.10  
  - **015 DNS Domain Name** → adlab.local  
- Authorized DHCP and verified DNS functionality

---

## 📁 03-GPOs  
**Screenshots stored in:** `03-GPOs`

### Group Policy Configurations:
#### ✔ Drive Mapping GPO  
- Created shared folders on the server  
- Built a **Drive Mapping** policy using Group Policy Preferences  
- Applied **Item-Level Targeting** using security groups  
- Verified group membership and share access via Computer Management

---

## 📁 04-ClientTesting  
**Screenshots stored in:** `04-ClientTesting`

### Validation Steps:
- Joined **client01** to the domain  
- Ran `gpupdate /force`  
- Verified applied GPOs using **RSOP** and **gpresult /r`**  
- Logged in as:  
  - **Brian Lopez**  
  - **Sarah Johnson**  
  - **Michael Reed**  
- Confirmed:
  - Correct drive mappings  
  - Correct folder permissions  
  - Working network authentication  
  - Proper access restrictions per user/group

---

## 🎯 Final Result

A fully functional Active Directory environment was created with:

- Windows Server 2019 domain controller  
- DHCP & DNS properly configured  
- Users, Groups, and OU structure  
- Drive Mapping GPO with item-level targeting  
- Successful client-side validation  

This lab simulates real enterprise sysadmin and helpdesk responsibilities.
