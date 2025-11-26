# 🛠️ Lab 02 – Remote Troubleshooting & Support Workflow

This lab simulates a real Helpdesk scenario where a remote user loses access to a shared network drive. The goal is to recreate the issue, diagnose it, fix it, and document a support workflow that reflects real enterprise troubleshooting.

---

## 📁 Screenshots  
All screenshots for this lab are stored in:  
**`Screenshots/`**

---

## 🧩 Overview

In this lab, I walked through a full end-to-end troubleshooting process:

- Recreated a shared drive issue  
- Validated network connectivity  
- Checked permissions and authentication  
- Applied fixes on the server  
- Confirmed successful access restoration  

This lab demonstrates realistic helpdesk responsibilities including communication, diagnosis, and remote user support.

---

## 🥇 Step 1 — Create & Share a Network Folder (Server)

- Created a shared folder on the server  
- Configured NTFS and Share permissions  
- Documented initial working state  

---

## 🥈 Step 2 — Map the Network Drive (Client)

- Tested access from the client  
- Mapped the network share  
- Verified initial connection success  

---

## 🥉 Step 3 — Break Permissions to Simulate Issue

- Removed necessary NTFS permissions  
- Ensured the client could no longer access the drive  
- Reproduced a realistic “Access Denied” ticket scenario  

---

## 🔍 Step 4 — Troubleshoot (Client Side)

- Tested reachability via `ping`  
- Checked DNS resolution  
- Verified share visibility  
- Attempted re-authentication  
- Reviewed credential manager / cached credentials  

---

## 🛠️ Step 5 — Fix the Issue (Server Side)

- Restored correct NTFS permissions  
- Validated share-level permissions  
- Confirmed user group membership  
- Ensured proper inheritance  

---

## ✅ Step 6 — Confirm Resolution

- Client remapped and accessed the folder  
- Verified read/write access works  
- Documented final working state  

---

## 🎯 Final Result

A realistic helpdesk troubleshooting workflow was completed, demonstrating:

- Network share troubleshooting  
- Permissions diagnosis  
- User access restoration  
- Documentation and structured workflow  
- Clear communication steps useful for enterprise support teams  
