---
description: |
  Evil-WinRM utilise l'instrumentation de gestion Windows (WMI) pour vous donner un shell interactif sur l'hôte Windows.

  Command Reference:

  	Target IP: <IP>

  	Username: <user>

  	Password: <passwd>

command: |
  evil-winrm -i <IP> -u <user> -p <passwd>
items:
  - Password
  - Username
services:
  - WMI
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/Hackplayers/evil-winrm
---
