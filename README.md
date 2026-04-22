# Windows Systemcheck Scripts
![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B-blue) ![Windows Server](https://img.shields.io/badge/Windows%20Server-2016%2B-orange) ![Security](https://img.shields.io/badge/Security-Auditing-red) ![License](https://img.shields.io/badge/License-GPLv3-green)

This repository contains lightweight PowerShell scripts (one-liners) for rapid system auditing and health checks of Windows Servers and Domain Controllers. The scripts use modern CIM-instances for better performance and future-proof compatibility.

**Author:** Ing. Akif Calhan  
**Year:** 2024 - 2026  
**License:** GNU General Public License v3.0 (GPLv3)

---

## 📂 Included Scripts

1. **systemcheck-server.ps1**: General health check for member servers and standalone systems.
2. **systemcheck-dc.ps1**: Extended deep audit specifically for Active Directory Domain Controllers.

---

## 💻 Usage

These scripts are formatted as PowerShell one-liners using `Invoke-RestMethod`. Run them in an **elevated PowerShell window** (Run as Administrator).

### For Standard Servers
```powershell
irm "[https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-server.ps1](https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-server.ps1)" | iex
For Domain Controllers
PowerShell
irm "[https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-dc.ps1](https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-dc.ps1)" | iex
🔍 Features & Audit Details
🛠 General Audit (both scripts)
Build Info: OS Caption, Version, Build Number and CSName via CIM Instance.

Network: Full ipconfig /all output and current LOGONSERVER check.

Computerinfo: Detailed hardware and system information.

Storage: Drive letters, Filesystem, Size (GB), Free Space (GB) and Free Percentage.

Windows Updates: List of installed Hotfixes (KB-Articles), sorted by installation date.

Security: Firewall profile status (Domain/Private/Public) and Network Category.

Roles & Features: List of all currently installed Windows Features.

🛡 DC Specific Audit (Additional)
Domain Info: Current Domain details and Forest information.

FSMO Roles: Displays all 5 Operations Master roles via netdom.

AD Topology: Lists all Domain Controllers across all Sites with IP and OS info.

Trusts: Overview of established Active Directory Trust relationships.

Health Check: Integrated dcdiag in both Verbose and Quiet mode.

Database Size: Real-time calculation of the NTDS database file size (MB).

⚠️ Disclaimer
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
