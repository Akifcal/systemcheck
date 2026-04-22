# Windows Systemcheck Scripts
![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B-blue) ![Windows Server](https://img.shields.io/badge/Windows%20Server-2016%2B-orange) ![Security](https://img.shields.io/badge/Security-Auditing-red) ![License](https://img.shields.io/badge/License-GPLv3-green)

This repository contains lightweight PowerShell scripts (one-liners) for rapid system auditing and health checks of Windows Servers and Domain Controllers.

**Author:** Ing. Akif Calhan  
**Year:** 2024 - 2026  
**License:** GNU General Public License v3.0 (GPLv3)

---

## 📂 Included Scripts

1. **systemcheck-server.ps1**: General health check for member servers and standalone systems.
2. **systemcheck-dc.ps1**: Extended deep audit specifically for Active Directory Domain Controllers.

---

## 💻 Usage

Run these commands in an **elevated PowerShell window** (Run as Administrator).

### For Standard Servers
```powershell
irm "https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-server.ps1" | iex
```


For Domain Controllers
```powershell
irm "https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-dc.ps1" | iex
```

🔍 Features & Audit Details
🛠 General Audit (both scripts)
Build Info: OS Caption, Version, Build Number and CSName via CIM Instance.

Network: Full ipconfig /all output and current LOGONSERVER check.

Computerinfo: Detailed hardware and system information.

Storage: Drive letters, Filesystem, Size (GB), Free Space (GB) and Free Percentage.

Windows Updates: List of installed Hotfixes, sorted by installation date.

Security: Firewall profile status and Network Category.

Roles & Features: List of all currently installed Windows Features.

🛡 DC Specific Audit (Additional)
FSMO Roles: Displays all 5 Operations Master roles via netdom.

AD Topology: Lists all Domain Controllers across all Sites with IP and OS info.

Health Check: Integrated dcdiag in both Verbose and Quiet mode.

Database Size: Real-time calculation of the NTDS database file size (MB).

⚠️ Disclaimer
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY. See the LICENSE for more details.
