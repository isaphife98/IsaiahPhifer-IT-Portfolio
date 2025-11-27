# 🖥️ Lab 01 – Active Directory Environment Setup & User Management  
**Windows Server 2019 • AD DS • DNS • DHCP • OUs • Users • Groups • Client Join**

This lab demonstrates building a complete Active Directory environment from scratch and validating domain functionality with a Windows 10 client.

---

## 📁 **01-ServerSetup**  
**Screenshots stored in:** [01-ServerSetup](./01-ServerSetup)

### **Actions Performed:**
- Created a new VirtualBox VM  
- Attached the Windows Server 2019 ISO  
- Installed Windows Server and completed initial setup  
- Logged in as **Administrator**  
- Performed Server Manager initial configuration (computer name, static IP, timezone, etc.)

---

## 📁 **02-DHCP_DNS**  
**Screenshots stored in:** [02-DHCP_DNS](./02-DHCP_DNS)

### **Actions Performed:**
- Installed **AD DS**, **DNS**, and **DHCP** roles  
- Promoted server to a Domain Controller for **adlab.local**  
- Configured DNS Forward Lookup Zone  
- Created DHCP scope with required options:  
  - **003 Router:** 10.0.0.1  
  - **006 DNS Server:** 10.0.0.10  
  - **015 DNS Domain Name:** adlab.local  
- Authorized DHCP and validated DNS resolution  

---

## 📁 **03-User_and_Group_Creation**  
**Screenshots stored in:** [03-User_and_Group_Creation](./03-User_and_Group_Creation)

### **Actions Performed:**
- Created base OU structure  
- Created user accounts:  
  - Ashley Young  
  - Brian Lopez  
  - David Kim  
  - Michael Reed  
  - Sarah Jones  
  - Xavier Parker  
- Created security groups:  
  - **HR Department**  
  - **Helpdesk Team**  
  - **IT Admins**  
- Assigned users to the correct department security groups  

---

## 📁 **04-Client_Domain_Join**  
**Screenshots stored in:** [04-Client_Domain_Join](./04-Client_Domain_Join)

### **Actions Performed:**
- Created Windows 10 VM (`client01`)  
- Set DNS to point to domain controller (10.0.0.10)  
- Joined client01 to **adlab.local**  
- Verified domain login using test users  
- Confirmed correct DNS suffix, IP configuration, and user session  

---

## 🎯 **Final Result**
This lab produced a fully configured enterprise-style AD environment:

- Windows Server 2019 Domain Controller  
- Functional DNS & DHCP services  
- Organized OUs  
- Users and role-based security groups  
- A domain-joined Windows 10 client  
- Verified authentication and domain connectivity  
