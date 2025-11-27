# 🛠️ Lab 08 – Remote Troubleshooting & Support Workflow

This lab simulates a real Helpdesk ticket where a user suddenly loses access to a mapped shared drive. I recreated the issue, troubleshot it from both the client and server perspective, restored access, and documented every step with screenshots.

---

## 📁 Screenshots
All screenshots are stored in the folder:  
**[📂 Screenshots](Screenshots/)**

---

# 🧩 Overview
This lab demonstrates the full lifecycle of a Helpdesk support case:

- Recreated the shared drive issue  
- Verified client connectivity  
- Checked authentication & cached credentials  
- Identified and fixed server-side permissions  
- Restored connectivity  
- Documented the workflow for future reference  

---

# 🥇 Step 1 — Create & Share the Network Folder (Server)

Configured a shared folder on the domain controller and verified initial share/NTFS permissions.

📸 **Screenshots:**  
- 01_ServerShareSettings.png  
- 02_ServerIP.png  

---

# 🥈 Step 2 — Map the Network Drive (Client)

Confirmed that the client can initially access the shared folder and map it successfully.

📸 **Screenshots:**  
- 03_ClientAccessInitial.png  
- 04_MappedDriveWorking.png  

---

# 🥉 Step 3 — Break Permissions to Simulate an Issue

Permissions were intentionally removed to recreate an “Access Denied” support scenario.

📸 05_ServerPermissionsBroken.png  

When the user attempts to access the mapped drive:  
📸 06_ClientAccessError.png  

---

# 🔍 Step 4 — Troubleshoot the Issue (Client-Side)

Performed standard Helpdesk diagnostics:

### ✔️ Network Connectivity  
📸 07_PingServer.png  

### ✔️ Credential Manager Check  
📸 08_CredentialCheck.png  

### ✔️ UNC Path Test  
📸 09_ClientUNC_Test.png  

Results showed:  
- Network is working  
- DNS is resolving  
- No cached credentials  
- UNC path reachable  
➡️ **Root cause confirmed: server-side permissions.**

---

# 🛠️ Step 5 — Fix the Issue (Server-Side)

Restored proper share + NTFS permissions and confirmed correct security group access.

📸 10_ServerPermissionsFixed.png  

---

# ✅ Step 6 — Confirm Resolution

The client tested again and successfully accessed the restored shared drive
