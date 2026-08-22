<h1 align="center">Hi, I'm Avery! 👋</h1>

<h3 align="center">Digital Artist | Windows Tweaker | Scripting & Tech Enthusiast</h3>

<br>

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=RikoTheDemonHunter&style=for-the-badge&color=7c3aed" alt="Profile Views" />
</div>

<br>

### 🚀 About Me
I'm a digital creator and power-user focused on custom OS debloating, low-level system optimization, automation, and digital art. I like squeezing maximum performance out of low-end and budget hardware through registry tweaks, customized Windows ISO builds, and lightweight scripts.

- 🎨 **Creative Work:** Digital art, animation edits, and channel design for *AveryArtz*.
- ⚡ **Tech Specialization:** Windows 10/11 debloating, Ghost Spectre setups, hardware repairs, and scripting.
- 🎮 **Gaming & Logic:** Complex redstone automation in Minecraft & strategic gaming.
- 🎓 **Current Journey:** Deepening my IT foundation and automation skills.

---

### 🛠️ Windows Debloating & Optimization Hub

#### 🔹 Essential Tools & Links
* **Bootable USB Creation:** Download [Rufus Official](https://rufus.ie/) to create lightweight, customized Windows boot drives (bypasses TPM/RAM requirements easily).
* **PowerShell Debloaters:** 
  * [Chris Titus Tech's Windows Utility](https://github.com/ChrisTitusTech/winutil) – Fast, GUI-driven debloating script.
  * [Win11Debloat](https://github.com/Raphire/Win11Debloat) – Lightweight PowerShell script to purge telemetry and preinstalled bloatware.

---

#### ⚡ Quick Scripting Snippets

**1. Purge Pre-installed AppX Packages (PowerShell - Admin)**
Remove non-essential Windows bloatware for current and new user profiles:
```powershell

:: Stop and disable telemetry services
sc stop DiagTrack
sc config DiagTrack start= disabled
sc stop dmwappushservice
sc config dmwappushservice start= disabled

:: Disable Connected User Experiences and Telemetry via Registry
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\DataCollection" /v AllowTelemetry /t REG_DWORD /d 0 /f






# Remove built-in bloatware applications
Get-AppxPackage -AllUsers | Where-Object {$_.Name -notlike "*Store*" -and $_.Name -notlike "*Calculator*"} | Remove-AppxPackage -ErrorAction SilentlyContinue
Get-AppxProvisionedPackage -Online | Where-Object {$_.DisplayName -notlike "*Store*" -and $_.DisplayName -notlike "*Calculator*"} | Remove-AppxProvisionedPackage -Online -ErrorAction SilentlyContinue
<!---
RikoTheDemonHunter/RikoTheDemonHunter is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
