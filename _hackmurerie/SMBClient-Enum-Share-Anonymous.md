---
description: |
  Smbclient est un outil utilisé pour communiquer avec les serveurs SMB. La commande suivante permet de se connecter à un partage SMB `<public>` en utilisant un login anonyme.

  Command Reference:

  	Target IP: <IP>

  	Domain: <domain.local>

  	SMB Share: <public>

command: |
  smbclient \\\\<domain.local>\\<public> -I <IP> -N
items:
  - No_Creds
  - Approved_Tool
  - Testing_Tool
  - New_Tool
services:
  - SMB
OS:
  - Linux
  - Approved_Tool
  - Testing_Tool
  - New_Tool
attack_types:
  - Enumeration
  - Approved_Tool
  - Testing_Tool
  - New_Tool
references:
  - https://www.samba.org/samba/docs/current/man-html/smbclient.1.html
  - https://www.madirish.net/59
---
