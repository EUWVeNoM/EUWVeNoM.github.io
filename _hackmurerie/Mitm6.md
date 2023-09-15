---
description: |
  Mitm6 est un outil de pentesting qui exploite la configuration par défaut de Windows pour prendre le contrôle du serveur DNS par défaut. Pour ce faire, il répond aux messages DHCPv6, fournit aux victimes une adresse IPv6 locale et définit l'hôte de l'attaquant comme serveur DNS par défaut. La commande suivante répondra aux messages DHCPv6 et définira le serveur DNS sur l'IP de l'hôte de l'attaque. Utilisez cette commande avec ntlmrelayx.py pour capturer les requêtes de configuration WPAD.

  Command Reference:

  	Domain: test.local

command: |
  mitm6 -d test.local --ignore-nofqnd
items:
  - No_Creds
services:
  - DNS
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/dirkjanm/mitm6
  - https://dirkjanm.io/worst-of-both-worlds-ntlm-relaying-and-kerberos-delegation/
---
