# Password Policy GPO

## 🎯 Objective
Configure and enforce strong password security settings across the entire domain.

## 🛠️ What I Configured
- Minimum password length  
- Maximum password age  
- Password history (preventing reuse)  
- Password complexity requirements  
- Account lockout parameters  

## 🧪 Validation & Testing
- Ran `gpupdate /force` on CLIENT01  
- Used `rsop.msc` to verify the policy  
- Confirmed the Default Domain Policy reflected updated password rules  

## 🧠 Skills Demonstrated
- Group Policy Management  
- Domain security hardening  
- Troubleshooting GPO inheritance and enforcement  
- Understanding industry password policy requirements  

## 📁 Screenshots
(Upload into `/GPO-Labs/PasswordPolicy/screenshots/`)
