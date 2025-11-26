# Lab 04 – Group Policy Configuration (GPO-Only Lab)
**Active Directory • GPO • System Hardening • Windows Management**

This lab focuses exclusively on creating and deploying **Group Policy Objects (GPOs)** in a Windows domain environment.

It demonstrates three critical enterprise policies used daily by Helpdesk, SysAdmin, and Security teams:

- **Password & Lockout Policy**  
- **Wallpaper Enforcement Policy**  
- **Block CMD Security Policy**

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
[Step01_Password_And_Lockout_Policy](Step01_Password_And_Lockout_Policy/)

---

# Step 02 -- Desktop Wallpaper Policy

This step applies a domain-wide desktop background using Group Policy.\
The wallpaper is stored in a shared folder on DC01 and delivered to all
domain users through GPO.

------------------------------------------------------------------------

📁 **Screenshots:**

[Step02_Wallpaper_Policy](./Step02_Wallpaper_Policy)

---

## 🖼️ 2.1 -- Place Wallpaper in Shared Folder on DC01

Copied custom wallpaper:

    C:\Wallpapershare\background.jpg

Configured share permissions: - Everyone → Read - NTFS permissions allow
read access for domain users

------------------------------------------------------------------------

## 🖥️ 2.2 -- Create & Configure the Wallpaper GPO

Created new GPO:

**ADLAB -- Desktop Wallpaper Policy**

Configured:

**User Configuration → Administrative Templates → Desktop → Desktop
Wallpaper**

Settings applied:

-   Enabled
-   Wallpaper Name (UNC path):

```{=html}
<!-- -->
```
    \\DC01.adlab.local\Wallpapershare\background.jpg

-   Wallpaper Style: Fill

------------------------------------------------------------------------

## 🔄 2.3 -- Apply the Policy

On the client (`client01`), forced policy update:

    gpupdate /force

Logged out and back in for settings to take effect.

------------------------------------------------------------------------

## 🌄 2.4 -- Verify Wallpaper on Client

The wallpaper successfully updated to the custom image across the domain
user session.

------------------------------------------------------------------------

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
[Step03_Block_CMD](Step03_Block_CMD/)

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
