---
description: |
  Le fichier ntlmrelayx.py d'Impacket effectue des attaques de relais NTLM, en créant un serveur SMB et HTTP et en relayant les informations d'identification vers différents protocoles (SMB, HTTP, LDAP, etc.).

  La commande ci-dessous crée un serveur relais SMB qui cible l'adresse IP 10.10.10.1, ce qui signifie que toutes les informations d'identification reçues par le serveur SMB sont relayées vers cette adresse IP pour tenter de s'authentifier et de créer une connexion de type sock à l'hôte. Pour que le serveur SMB reçoive des informations d'identification à relayer, dementor.py ou Petitpotam peuvent être utilisés pour déclencher une authentification forcée de l'IP ciblée vers un serveur SMB contrôlé par l'attaquant.

  Command Reference:

  	Target IP: 10.10.10.1

command: |
  python3 ntlmrelayx.py -smb2support -t smb://10.10.10.1 -socks
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/ntlmrelayx.py
  - https://www.praetorian.com/blog/active-directory-computer-account-smb-relaying-attack
---
