# Lab 06 📡 Printer Deployment via Group Policy (GPO)

Lab Type: Active Directory | Group Policy | Print Management
Server: Windows Server 2019 (DC01)
Client: Windows 10 (client01)
Objective: Create a shared network printer on DC01 and deploy it automatically to domain users using Group Policy.

## 🧩 Overview

In this lab, I:

- Installed a virtual printer on the domain controller (DC01)
- Shared the printer for domain users
- Created a Printer Deployment GPO
- Configured Point and Print Restrictions
- Linked the GPO to the Users OU
- Verified automatic deployment on client01

This replicates a real helpdesk task where IT support must deploy network printers to all users without manually installing them.

```

## 🥇 Step 01 — Create & Share the Printer on DC01

1. Open Devices and Printers  
2. Add a printer  
3. Select manual configuration  
4. Choose LPT1  
5. Install Generic/Text Only driver  
6. Name: **IT Department Printer – PDF**  
7. Enable printer sharing  
8. Confirm printer appears on DC01  

## 🥈 Step 02 — Deploy Printer via GPO

1. Create GPO: **Printer Deployment Policy**  
2. Add shared printer under Deployed Printers  
3. Link GPO to **Users** OU  
4. Configure Point and Print Restrictions  

## 🥉 Step 03 — Client Validation (client01)

1. Run `gpupdate /force`  
2. Run `gpresult /r`  
3. Open `\\DC01`  
4. Confirm printer installed in Devices and Printers  

## 🎉 Results

✔ Printer successfully created and shared  
✔ Deployed via Group Policy  
✔ Automatically installed on client machine  
✔ Fully validated  

## 🧠 Skills Demonstrated

- AD OU administration  
- Group Policy configuration  
- Printer deployment  
- Troubleshooting  
- Documentation  
