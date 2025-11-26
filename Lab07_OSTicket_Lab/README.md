# Lab 07 🎫 osTicket Helpdesk Lab

This lab walks through installing and configuring the **osTicket** helpdesk system on a Windows 10 VM using **XAMPP** and **MySQL**, then simulates real-world tickets from end users and resolves them as an IT support agent.

---

## 💻 Lab Environment

- **Host:** Windows 10 Pro (VirtualBox)  
- **Web stack:** XAMPP (Apache + MySQL + PHP)  
- **Helpdesk:** osTicket v1.18.2  
- **Database:** MySQL (utf8mb4_general_ci)  
- **Browser:** Chrome  

---

## 🧠 Skills Demonstrated

- Installing and configuring a PHP web application (osTicket)  
- Managing MySQL databases and collation in phpMyAdmin  
- Editing application configuration files  
- Configuring helpdesk settings, company profile, and email templates  
- Creating departments, teams, and agents to mirror IT support structure  
- Using the end-user portal to submit tickets  
- Working tickets as an agent: assignment, communication, and resolution  

---

## 📁 01-Installation  
**Screenshots stored in:**  
[01-Installation](01-Installation/)

Includes:
- XAMPP installation  
- Starting Apache & MySQL  
- Accessing phpMyAdmin  
- Extracting and placing osTicket files  

---

## 📁 02-Database-Setup  
**Screenshots stored in:**  
[02-Database-Setup](02-Database-Setup/)

Includes:
- Creating the osTicket database  
- Setting **utf8mb4_general_ci**  
- Verifying tables after installation  

---

## 📁 03-Admin-Configuration  
**Screenshots stored in:**  
[03-Admin-Configuration](03-Admin-Configuration/)

Includes:
- Running the osTicket installer  
- Editing the config file  
- Admin dashboard setup  
- Company info, email templates, SLAs  

---

## 📁 04-Departments-Teams-Agents  
**Screenshots stored in:**  
[04-Departments-Teams-Agents](04-Departments-Teams-Agents/)

Includes:
- IT Support Department  
- Tier 1 Team  
- Agent creation & role assignment  

---

## 📁 05-User-Portal  
**Screenshots stored in:**  
[05-User-Portal](05-User-Portal/)

Includes:
- End-user portal homepage  
- Submitting Ticket #1 & Ticket #2  
- Auto-responder emails  

---

## 📁 06-Ticket-Workflow  
**Screenshots stored in:**  
[06-Ticket-Workflow](06-Ticket-Workflow/)

Includes:
- Agent dashboard  
- Claiming and assigning tickets  
- Responding, updating, resolving  
- Closing ticket lifecycle  

---

## 🏁 Summary

This lab demonstrates the full lifecycle of deploying and using a helpdesk application:

1. Installing and configuring the web stack (XAMPP).  
2. Creating and preparing a MySQL database.  
3. Installing and configuring osTicket.  
4. Building helpdesk structure with departments, teams, and agents.  
5. Submitting tickets as users and resolving them as IT support.  
