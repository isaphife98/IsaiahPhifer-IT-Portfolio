# Lab 05 – Printer Deployment via Group Policy (GPO)
**Active Directory • GPO • Print Services • Client Management**

This lab demonstrates how to deploy a shared printer to domain‑joined clients using **Group Policy Preferences**, one of the most common tasks performed by Helpdesk and SysAdmin teams.

---

## 📁 Step 01 — Create & Share the Printer on DC01
**Screenshots stored in:**  
[Step 01 — Create & Share the Printer on DC01](Step%2001%20%E2%80%94%20Create%20%26%20Share%20the%20Printer%20on%20DC01/)

### Actions Performed:
- Installed a virtual printer (Microsoft XPS Document Writer / PDF printer)
- Shared the printer from **DC01**
- Set share name, permissions, and drivers
- Confirmed network visibility

---

## 📁 Step 02 — Deploy Printer via Group Policy
**Screenshots stored in:**  
[Step 02 — Deploy Printer via Group Policy](Step%2002%20%E2%80%94%20Deploy%20Printer%20via%20Group%20Policy/)

### GPO Used:
**“Printer Deployment GPO”**

Configured via:

```
Computer Configuration
   → Policies
        → Windows Settings
             → Deployed Printers
```

or

```
User Configuration
   → Preferences
        → Control Panel Settings
             → Printers
```

### Deployment Details:
- Assigned the shared printer automatically
- Linked GPO to correct OU
- Forced update with **gpupdate /force**

---

## 📁 Step 3 — Client Validation (client01)
**Screenshots stored in:**  
[Step 3 — Client Validation (client01)](Step%203%20%E2%80%94%20Client%20Validation%20(client01)/)

### Validated:
- Printer appears under **Control Panel → Devices & Printers**
- Printer functions as default or available device
- Confirmed:
  - GPO applied successfully  
  - Printer reachable on network  
  - Permissions enforced correctly  

---

## 🧠 Summary

This lab demonstrates:

- Creating & sharing printers on Windows Server
- Deploying printers using **Group Policy Preferences**
- Automatic printer assignment to domain users
- Validation across client machines
- Real‑world print management workflow

A key Helpdesk and SysAdmin responsibility in enterprise environments.

