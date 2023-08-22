---
description: |
  "CrackMapExec (alias CME) est un outil de post-exploitation qui permet d'automatiser l'évaluation de la sécurité des grands réseaux Active Directory." - https://github.com/mpgn/CrackMapExec/wiki. La commande suivante énumère une liste d'hôtes SMB dont la signature n'est pas appliquée, ce qui vous permet de leur transmettre des informations d'identification à l'aide de ntlmrelayx.py.

  Command Reference:

  	SMB Hosts: <smb-hosts.txt>

command: |
  crackmapexec smb <smb-hosts.txt> --gen-relay-list output.txt
items:
  - No_Creds
services:
  - SMB
attack_types:
  - Enumeration
OS:
  - Linux
references:
  - https://github.com/mpgn/CrackMapExec
  - https://github.com/mpgn/CrackMapExec/wiki
---
