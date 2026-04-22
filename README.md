# Windows Systemcheck Scripts
![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B-blue) ![Windows Server](https://img.shields.io/badge/Windows%20Server-2016%2B-orange) ![License](https://img.shields.io/badge/License-GPLv3-green)

This repository contains lightweight PowerShell one-liners for rapid system auditing and health checks of Windows Servers and Domain Controllers.

**Author:** Ing. Akif Calhan  
**Year:** 2024 - 2026  
**License:** GNU General Public License v3.0 (GPLv3)

---

## 🛠 Included Scripts

1. **Systemcheck Server:** General health check for member servers and standalone systems.
2. **Systemcheck Domain Controller:** Deep audit for DCs including FSMO roles, AD replication, and dcdiag.

---

## 💻 Usage

Run these commands in an **elevated PowerShell window** (Run as Administrator).

### For Standard Servers
```powershell
irm "[https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-server.ps1](https://raw.githubusercontent.com/Akifcal/systemcheck/main/systemcheck-server.ps1)" | iex
