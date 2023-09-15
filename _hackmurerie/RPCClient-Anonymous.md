---
description: |
  Rpcclient est un outil utilisé pour exécuter des fonctions MS-RPC côté client afin de gérer les clients Windows NT à partir de postes de travail Unix. Du point de vue de la sécurité offensive, il peut être utilisé pour énumérer les utilisateurs, les groupes et d'autres informations potentiellement sensibles. La commande suivante tente de se connecter au serveur NetBIOS de manière anonyme, afin d'énumérer les commandes/fonctions MS-RPC disponibles.

  Command Reference:

  	Target IP: 10.10.10.1

command: |
  rpcclient -U '' -N 10.10.10.1
items:
  - No_Creds
services:
  - RPC
OS:
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html
  - https://www.ired.team/offensive-security/enumeration-and-discovery/enumerating-windows-domains-using-rpcclient-through-socksproxy-bypassing-command-line-logging
---
