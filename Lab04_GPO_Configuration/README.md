# Lab 04 Group Policy Configuration (GPO-Only Lab)
**Active Directory • GPO • System Hardening • Windows Management**

This lab focuses exclusively on creating and deploying **Group Policy Objects (GPOs)** in a Windows domain environment.

It demonstrates three critical enterprise policies used daily by Helpdesk, SysAdmin, and Security teams:

- **Password & Lockout Policy**  
- **Wallpaper Enforcement Policy**  
- **Block CMD Security Policy**

This lab isolates your GPO skills so recruiters can clearly see your policy engineering ability without mixing it into AD setup, NTFS permissions, or drive mapping.

---

## 📌 Objectives

- Modify Password & Lockout policy inside **Default Domain Policy**  
- Deploy an organization-wide wallpaper using **NETLOGON**  
- Block Command Prompt for non-admin users  
- Verify GPO application via `gpupdate` & `gpresult`  
- Test across multiple client machines and accounts  

---

## 🟦 Step 01 – Password & Account Lockout Policies

**Implemented policies:**

- Minimum password length  
- Password complexity  
- Maximum password age  
- Account lockout threshold  
- Lockout duration  
- Reset timeframe  

**Validation performed:**

- `gpupdate /force`  
- `gpresult /r`  
- GPMC view of GPO links & applied settings  

📁 **Screenshots:**  
`Step01_Password_And_Lockout_Policy/`

---

## 🟦 Step 02 – Desktop Wallpaper Policy

**Steps completed:**

1. Copied custom wallpaper to:  
   `\\DC01\NETLOGON\wallpaper.jpg`
2. Created new GPO:  
   **Organization Wallpaper Policy**
3. Configured:  
   `User Configuration → Admin Templates → Desktop → Desktop Wallpaper`
4. Verified correct path & display mode  
5. Forced GPO update on client  
6. Confirmed wallpaper applied correctly  

📁 **Screenshots:**  
`Step02_Wallpaper_Policy/`

---

## 🟦 Step 03 – Block CMD Policy (Security Hardening)

**Configuration:**

`User Configuration → Administrative Templates → System → Prevent access to the command prompt`

Settings:

- Enabled policy  
- Disabled script execution as an added restriction  

**Testing:**

- Ran `gpupdate /force`  
- Opened CMD on client  
- Verified block message  
- Confirmed policy enforcement across users  

📁 **Screenshots:**  
`Step03_Block_CMD/`

---

## 📘 Summary

This lab demonstrates essential Windows enterprise administration skills:

- Editing the **Default Domain Policy**  
- Deploying domain-wide GPOs  
- Linking policies to specific OUs  
- Using **NETLOGON** for enterprise-file distribution  
- Validating GPO results on clients  
- System hardening through policy enforcement  

This isolated GPO lab helps your portfolio stand out by proving you can **design, deploy, and validate real-world Group Policy configurations** used across corporate environments.
