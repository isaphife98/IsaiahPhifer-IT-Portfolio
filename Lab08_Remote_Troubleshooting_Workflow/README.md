# 🛠️ Lab 08 – Remote Troubleshooting & Support Workflow

This lab simulates a real Helpdesk ticket where a user suddenly loses access to a mapped shared drive. I recreated the issue, troubleshot it from both the client and server side, restored access, and documented each step.

---

## 📁 Screenshots  
All screenshots are stored in the folder:  
**[📂 Screenshots](Screenshots/)**

---

# 🧩 Overview  
This lab demonstrates an end-to-end troubleshooting workflow:

- Recreated the shared drive issue  
- Verified client connectivity  
- Checked authentication and cached credentials  
- Identified the root cause  
- Corrected server-side permissions  
- Restored user access  
- Documented every step for helpdesk use  

---

# 🥇 Step 1 — Create & Share the Network Folder (Server)

Configured a shared folder on the domain controller and verified initial permissions.

📸 **Screenshots:**  
- [01_ServerShareSettings.png](Screenshots/01_ServerShareSettings.png)  
- [02_ServerIP.png](Screenshots/02_ServerIP.png)

---

# 🥈 Step 2 — Map the Network Drive (Client)

Confirmed the client can access the share and map it successfully.

📸 **Screenshots:**  
- [03_ClientAccessInitial.png](Screenshots/03_ClientAccessInitial.png)  
- [04_MappedDriveWorking.png](Screenshots/04_MappedDriveWorking.png)

---

# 🥉 Step 3 — Break Permissions to Simulate an Issue

Permissions were intentionally removed to recreate a realistic “Access Denied” scenario.

📸 **Screenshots:**  
- [05_ServerPermissionsBroken.png](Screenshots/05_ServerPermissionsBroken.png)  
- [06_ClientAccessError.png](Screenshots/06_ClientAccessError.png)

---

# 🔍 Step 4 — Troubleshoot the Issue (Client-Side)

Performed standard Helpdesk diagnostics.

### ✔️ Network Connectivity  
📸 [07_PingServer.png](Screenshots/07_PingServer.png)

### ✔️ Credential Manager Check  
📸 [08_CredentialCheck.png](Screenshots/08_CredentialCheck.png)

### ✔️ UNC Path Test  
📸 [09_ClientUNC_Test.png](Screenshots/09_ClientUNC_Test.png)

Findings:  
- Network connectivity OK  
- DNS resolving correctly  
- No cached credentials  
- UNC path reachable  
➡️ Issue confirmed to be server-side permissions.

---

# 🛠️ Step 5 — Fix the Issue (Server-Side)

Restored correct **NTFS** and **share permissions**.

📸 **Screenshot:**  
- [10_ServerPermissionsFixed.png](Screenshots/10_ServerPermissionsFixed.png)

---

# ✅ Step 6 — Confirm Resolution

Client re-tested access and successfully opened the shared drive.

📸 **Screenshot:**  
- [11_ClientAccessRestored.png](Screenshots/11_ClientAccessRestored.png)

---

# 🎯 Final Result

This lab demonstrates real enterprise troubleshooting including:

- Network share diagnostics  
- Permission & authentication verification  
- Accurate root-cause identification  
- Systematic helpdesk-style workflow  
- Clear communication & documentation  
