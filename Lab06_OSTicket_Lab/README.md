# 🎫 osTicket Helpdesk Deployment & Ticket Workflow Lab  
**Windows 10 • XAMPP • MySQL • PHP • Helpdesk Administration**

This lab demonstrates a full end-to-end deployment of the **osTicket Helpdesk System**, including installation, database setup, helpdesk configuration, user portal usage, and ticket resolution from the IT agent perspective.

---

## 🛠️ Lab Environment

- **Host OS:** Windows 10 Pro (VirtualBox)  
- **Web Stack:** XAMPP (Apache, MySQL, PHP)  
- **Helpdesk System:** osTicket v1.18.2  
- **Database Engine:** MySQL (utf8mb4_general_ci)  
- **Browser:** Google Chrome  

---

## 🧩 Skills Demonstrated

- Installing & configuring a full PHP web application (osTicket)  
- Creating MySQL databases, users, and collation standards via phpMyAdmin  
- Editing & securing osTicket configuration files  
- Building helpdesk structure: departments, teams, and agents  
- Setting SLA, ticket routing, and system-wide admin settings  
- Submitting tickets as an end user  
- Working tickets as an IT agent: assignment, communication, resolution  

---

# 📁 Step 01 — Installation  
**Screenshots stored in:**  
➡️ [01-Installation](01-Installation)

### **Actions Performed**
- Installed **XAMPP** (Apache, MySQL, PHP)  
- Verified localhost + phpMyAdmin access  
- Extracted and deployed the osTicket package to `C:\xampp\htdocs\osticket`  
- Enabled required PHP extensions  
- Launched the osTicket web installer  

---

# 📁 Step 02 — Database Setup  
**Screenshots stored in:**  
➡️ [02-Database-Setup](02-Database-Setup)

### **Actions Performed**
- Created MySQL database: **osticket**  
- Set collation: **utf8mb4_general_ci**  
- Created a dedicated MySQL user w/ privileges  
- Confirmed tables generated during installation  

---

# 📁 Step 03 — Admin Configuration  
**Screenshots stored in:**  
➡️ [03-Admin-Configuration](03-Admin-Configuration)

### **Actions Performed**
- Completed osTicket installer  
- Configured helpdesk name, URL, and system email  
- Adjusted company profile & ticket settings  
- Customized email templates and auto-responses  
- Verified admin dashboard functionality  

---

# 📁 Step 04 — Departments, Teams & Agents  
**Screenshots stored in:**  
➡️ [04-Departments-Teams-Agents](04-Departments-Teams-Agents)

### **Actions Performed**
- Created **IT Support** department  
- Added **Tier 1 Support** team  
- Created helpdesk agents (tech accounts)  
- Set roles, permissions, and ticket assignment rules  

---

# 📁 Step 05 — User Portal & Ticket Submission  
**Screenshots stored in:**  
➡️ [05-User-Portal](05-User-Portal)

### **Actions Performed**
- End user accessed **/osticket** portal  
- Submitted test tickets (#1 and #2)  
- Verified email confirmation & ticket visibility  
- Captured user-side ticket creation flow  

---

# 📁 Step 06 — Ticket Workflow (Agent Perspective)  
**Screenshots stored in:**  
➡️ [06-Ticket-Workflow](06-Ticket-Workflow)

### **Actions Performed**
- Logged in as agent  
- Viewed newly created tickets  
- Assigned tickets to self  
- Responded with troubleshooting steps  
- Set ticket status → resolved  
- Closed ticket and verified user notification  

---

## ✅ Summary

This lab demonstrates the **full lifecycle of deploying and using a helpdesk platform**:

1. Installed and configured XAMPP  
2. Created and prepared MySQL database  
3. Deployed osTicket and confirmed system functionality  
4. Built helpdesk structure: departments, teams, agents  
5. Submitted tickets via end-user portal  
6. Fully processed tickets as an IT support agent  

This mirrors real-world requirements for **IT Helpdesk, System Administrator, and Technical Support** roles.
