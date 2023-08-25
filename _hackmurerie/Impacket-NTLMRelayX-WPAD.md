---
description: |
  Le fichier ntlmrelayx.py d'Impacket effectue des attaques de relais NTLM, en créant un serveur SMB et HTTP et en relayant les informations d'identification vers différents protocoles (SMB, HTTP, LDAP, etc.).

  La commande ci-dessous effectue une usurpation de WPAD pour forcer la machine victime à s'authentifier auprès de l'hôte contrôlé par l'attaquant. La commande relaie ensuite l'authentification pour créer un nouvel objet informatique et lui accorder des droits de délégation afin d'usurper l'identité d'utilisateurs sur la machine victime. Cette commande doit être utilisée conjointement avec mitm6.

  Command Reference:

  	Target Domain Controller: dc.test.local

command: |
  python3 ntlmrelayx.py -t ldaps://dc.test.local -wh test-wpad --delegat-access
items:
  - No_Creds
services:
  - NTLM
  - LDAP
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/ntlmrelayx.py
  - https://dirkjanm.io/worst-of-both-worlds-ntlm-relaying-and-kerberos-delegation/
---
