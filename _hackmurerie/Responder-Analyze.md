---
description: |
  Responder est un empoisonneur LLMNR, NBT-NS et MDNS. Il répond aux requêtes NBT-NS (NetBIOS Name Service) spécifiques basées sur le suffixe de leur nom. Par défaut, l'outil ne répondra qu'aux requêtes du service de serveur de fichiers, qui est pour SMB. La commande suivante mettra Responder en mode analyse, écoutant les requêtes NBT-NS, BROWSER et LLMNR sans y répondre.

  Command Reference:

  	Interface: eth0

command: |
  Responder -I eth0 -A
items:
  - No_Creds
services:
  - NTLM
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/lgandx/Responder
  - https://www.ivoidwarranties.tech/posts/pentesting-tuts/responder/cheatsheet/
---
