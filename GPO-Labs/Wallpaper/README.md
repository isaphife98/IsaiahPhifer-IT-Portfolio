# Desktop Wallpaper GPO

## 🎯 Objective
Force a custom company wallpaper across all domain workstations using Group Policy.

## 🛠️ What I Configured
- Created a shared network folder containing the wallpaper  
- Configured the “Desktop Wallpaper” GPO setting  
- Linked GPO to the **Workstations OU**  
- Set policy to prevent users from changing the wallpaper  

## 🧪 Validation & Testing
- Ran `gpupdate /force`  
- Verified wallpaper applied on CLIENT01  
- Confirmed the policy source via `gpresult`  

## 🧠 Skills Demonstrated
- GPO Preferences  
- UNC path management  
- Policy enforcement  
- Desktop environment standardization  

## 📁 Screenshots
(Upload into `/GPO-Labs/Wallpaper/screenshots/`)
