---
description: |
  TargetedKerberoast est un script Python qui peut, comme beaucoup d'autres (par exemple GetUserSPNs.py), imprimer les hashs "kerberoast" pour les comptes utilisateurs qui ont un SPN défini. Cet outil apporte la fonctionnalité supplémentaire suivante : pour chaque utilisateur sans SPN, il tente d'en définir un (abus d'une permission d'écriture sur l'attribut servicePrincipalName), imprime le hash "kerberoast", et supprime le SPN temporaire défini pour cette opération.

  Command Reference:

  	Target IP: 10.10.10.1

  	Attacker IP: 10.10.10.2

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 targetedKerberoast.py -d test.local -u john -p password123 --dc-ip 10.10.10.1
items:
  - Password
  - Username
services:
  - Kerberos
  - NTLM
OS:
  - Linux
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/ShutdownRepo/targetedKerberoast
---
