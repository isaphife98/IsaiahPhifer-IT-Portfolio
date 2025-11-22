# NTFS Permissions Lab

This lab demonstrates setting up NTFS and share permissions using best practices: group-based access, least privilege, and testing access with domain users.

---

## 🧰 Tools & Technologies
- Windows Server 2019  
- Windows 10 (Client01)  
- Active Directory Users & Computers  
- NTFS Permissions  
- Shared Folders

---

## 🛠️ What I Completed
### ✔ Created Shared Folders
- HR  
- Helpdesk  
- IT  
- Public  

### ✔ Applied NTFS permissions using security groups:
Example:
- HR folder → HR-Group = Modify  
- Helpdesk folder → Helpdesk-Group = Modify  
- IT folder → IT-Admins = Full Control  
- Public folder → Everyone = Read  

### ✔ Added domain users to correct groups
### ✔ Tested permission access from Client01
- Verified allowed access  
- Verified denied access  
- Confirmed group-based authorization  

---

## 📸 Screenshots
Store in `/NTFS-Permissions-Lab/screenshots`:
- Folder creation  
- Security tab permissions  
- Group membership  
- User access tests  

---

## 🎯 Skills Demonstrated
- NTFS permissioning  
- Access control  
- Group-based security management  
- Realistic helpdesk troubleshooting  

---

## 📁 Folder Layout
```
NTFS-Permissions-Lab/
│
├── screenshots/
└── README.md
```

---

## ✅ Status
**Completed**
