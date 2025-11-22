# Password Policy GPO

## 🎯 Objective
Configure and enforce strong password security settings across the entire domain.

---

## ✅ What I Configured

- Minimum password length
- Maximum password age
- Password history (preventing recent reuse)
- Password complexity requirements
- Account lockout-related parameters

I applied these via Group Policy and ensured they were linked and enforced at the domain level.

---

## 🧪 Validation & Testing

- Ran `gpupdate /force` on CLIENT01
- Opened **Resultant Set of Policy (rsop.msc)** to confirm the effective password settings
- Verified that the **Default Domain Policy** reflected the updated password rules

---

## 🧠 Skills Demonstrated

- Group Policy Management
- Domain-wide security hardening
- Understanding of password policy best practices
- Troubleshooting GPO inheritance and enforcement

---

## 📸 Screenshots

Store files in: `GPO-Labs/PasswordPolicy/screenshots/`

Suggested screenshots:
- Password policy settings in GPMC
- RSOP showing effective password settings

---

## 📁 Folder Layout

```text
GPO-Labs/PasswordPolicy/
├── screenshots/
└── README.md
