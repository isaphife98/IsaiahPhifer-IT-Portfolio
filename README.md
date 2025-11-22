# Isaiah Phifer – IT Support Portfolio

Welcome to my hands-on IT Support / Helpdesk portfolio.

I built this repository to document real homelab projects I used to develop skills in:

- Active Directory & Group Policy
- Windows Server administration
- File permissions & access control (NTFS & shares)
- Networking & troubleshooting (DNS, IP, routing)
- Ticketing systems & helpdesk workflows
- Remote troubleshooting and documentation

All labs were built locally on my own virtualized environment using VirtualBox, Windows Server 2019, and Windows 10.

---

## 🧪 Projects & Labs

### 1. Active Directory Lab
**Skills:** Domain Controller setup, DNS, OUs, security groups  
**Folder:** `ActiveDirectory-Lab/`

- Promoted a server to a Domain Controller and created the domain `adlab.local`.
- Built a clean OU structure for departments, users, and workstations.
- Created named domain users and assigned them to appropriate security groups (HR, Helpdesk, IT).
- Joined a Windows 10 workstation (CLIENT01) to the domain and tested logons with multiple users.

---

### 2. NTFS Permissions Lab
**Skills:** NTFS permissions, share rights, group-based security, least privilege  
**Folder:** `NTFS-Permissions-Lab/`

- Created departmental shared folders on a file server.
- Configured NTFS and share permissions using security groups instead of individual users.
- Implemented least-privilege access so HR, IT, and Helpdesk had the correct level of read/modify access.
- Verified access from CLIENT01 as different users and confirmed permission behavior.

---

### 3. Drive Mapping Lab (GPO)
**Skills:** Group Policy Preferences, drive mappings, automation  
**Folder:** `Drive-Mapping-Lab/`

- Created security groups for each department.
- Configured shared folders for HR, IT, and Helpdesk.
- Used Group Policy Preferences to automatically map network drives based on security group membership.
- Linked the GPO to the Workstations OU and verified mappings on CLIENT01 with different user accounts.

---

### 4. Group Policy Labs
**Skills:** GPO design, password policy, security hardening, user experience  
**Folder:** `GPO-Labs/`

Includes three focused GPO projects:

1. **Password Policy GPO** – enforced strong password rules domain-wide.  
2. **Block CMD GPO** – disabled Command Prompt for standard users to reduce abuse.  
3. **Desktop Wallpaper GPO** – deployed a standard corporate wallpaper to all workstations.

Each subfolder has its own README and screenshots.

---

### 5. Networking & Troubleshooting Lab
**Skills:** DNS troubleshooting, ping, tracert, nslookup, basic network diagnosis  
**Folder:** `Networking-Troubleshooting-Lab/`

- Used `ipconfig /all` to verify addressing and DNS configuration.
- Tested connectivity to the Domain Controller by IP, hostname, and FQDN.
- Ran `tracert` to confirm routing path to the server.
- Used `nslookup` to test DNS name resolution (both internal domain and external-style names).
- Simulated network issues (disabling adapter, wrong DNS) and verified failure/recovery.

---

### 6. Remote Troubleshooting Lab
**Skills:** Event Viewer analysis, system diagnostics, root cause analysis  
**Folder:** `Remote-Troubleshooting-Lab/`

- Reviewed Windows logs in Event Viewer to investigate application and system events.
- Checked performance and resource usage using Task Manager.
- Inspected services and startup configuration to identify contributing issues.
- Documented findings and resolution steps as if reporting back to a user or ticket.

---

### 7. OSTicket Helpdesk Project
**Skills:** Ticket lifecycle, SLA, helpdesk workflows, communication  
**Folder:** `OSTicket-Helpdesk-Project/`

- Installed and configured the OSTicket helpdesk platform.
- Created departments (IT, HR, Helpdesk) and configured agents and roles.
- Built SLAs and help topics to route tickets correctly.
- Walked multiple tickets through the full lifecycle: submission → triage → assignment → escalation → resolution → closure.
- Documented communication and troubleshooting throughout.

---

### 8. Helpdesk Simulation Project
**Skills:** Ticket handling, prioritization, written communication, escalation  
**Folder:** `Helpdesk-Simulation-Project/`

- Simulated real IT support tickets based on common end-user problems.
- Collected “user reports,” identified the most important details, and documented them clearly.
- Wrote step-by-step troubleshooting notes and resolutions.
- Practiced escalation and handoff between tiers while keeping user communication clear and professional.

---

## 🛠 Tools & Technologies

- **Operating Systems:** Windows Server 2019, Windows 10  
- **Directory Services:** Active Directory Domain Services (AD DS), DNS  
- **Management & Security:** Group Policy Management, NTFS, sharing  
- **Networking:** ipconfig, ping, tracert, nslookup, network adapter tools  
- **Troubleshooting:** Event Viewer, Task Manager, Services console  
- **Helpdesk:** OSTicket, ticket logging, documentation

---

## 🎯 Career Goal

My goal is to transition into an IT Support / Helpdesk Technician role and grow into cybersecurity over time by building on this hands-on experience.

---

## 📬 Contact

- **Email: isaphife@gmail.com  
- **LinkedIn:** *(add your LinkedIn profile URL here)*  

Thank you for viewing my portfolio.
