# Lab 06 📡 Printer Deployment via Group Policy (GPO)

Lab Type: Active Directory | Group Policy | Print Management  
Server: Windows Server 2019 (DC01)  
Client: Windows 10 (client01)  
Objective: Create a shared network printer on DC01 and deploy it automatically to domain users using Group Policy.

---

## 🧩 Overview

In this lab, I:

- Installed a virtual printer on the domain controller (DC01)  
- Shared the printer for domain users  
- Created a Printer Deployment GPO  
- Configured Point and Print Restrictions  
- Linked the GPO to the **Users OU**  
- Verified automatic deployment on **client01**

This replicates a real helpdesk task where IT must deploy network printers without manually installing them on individual computers.

---

## 🥇 Step 01 — Create & Share the Printer on DC01  
📁 **All screenshots stored in:**  
**`Step 01 — Create & Share the Printer on DC01`**

### Actions Performed:
1. Open **Devices and Printers**  
2. Add a new printer  
3. Select **Add a local printer or network printer with manual settings**  
4. Choose **LPT1** port  
5. Install the **Generic/Text Only** printer driver  
6. Name the printer **IT Department Printer – PDF**  
7. Enable **printer sharing**  
8. Confirm the printer appears in the list on DC01  

---

## 🥈 Step 02 — Deploy Printer via Group Policy  
📁 **All screenshots stored in:**  
**`Step 02 — Deploy Printer via Group Policy`**

### Actions Performed:
1. Create a new GPO called **Printer Deployment Policy**  
2. Add the shared printer under **Deployed Printers**  
3. Link the GPO to the **Users OU**  
4. Configure **Point and Print Restrictions** to allow installation without admin prompts  

---

## 🥉 Step 3 — Client Validation (client01)  
📁 **All screenshots stored in:**  
**`Step 3 — Client Validation (client01)`**

### Actions Performed:
1. Run `gpupdate /force` on client01  
2. Run `gpresult /r` to verify policy application  
3. Open `\\DC01` to view shared printers  
4. Confirm the printer automatically installs in **Devices and Printers**  

---

## 🎉 Results

✔ Printer successfully created and shared on DC01  
✔ Deployed domain-wide using Group Policy  
✔ Automatically installed on the client PC  
✔ Fully validated through gpupdate & gpresult  

---

## 🧠 Skills Demonstrated

- Active Directory OU management  
- Group Policy (GPO) creation and linking  
- Printer deployment automation  
- Troubleshooting & validation  
- Technical documentation  
