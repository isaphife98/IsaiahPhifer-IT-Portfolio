# Block CMD GPO (Disable Command Prompt)

## 🎯 Objective
Disable Command Prompt access for standard domain users to prevent unauthorized system-level commands and script execution.

## 🛠️ What I Configured
- Enabled **“Prevent access to the command prompt”**  
- Disabled **batch file processing**  
- Linked the GPO to the **Workstations OU**  
- Ensured it applied only to non-admin users  

## 🧪 Validation & Testing
- Ran `gpupdate /force`  
- Verified using `gpresult /r`  
- Attempted to open CMD on CLIENT01 (received “Blocked by Group Policy” message)

## 🧠 Skills Demonstrated
- Windows security hardening  
- User restriction policies  
- GPO scoping & filtering  
- Troubleshooting GPO application  

## 📁 Screenshots
(Upload into `/GPO-Labs/BlockCMD/screenshots/`)
