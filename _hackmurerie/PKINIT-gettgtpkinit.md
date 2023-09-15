---
description: |
  PKINIT gettgtpkinit.py demande un TGT en utilisant un fichier PFX, soit en tant que fichier, soit en tant que blob encodé en base64, ou des fichiers PEM pour cert+key. Ceci utilise Kerberos PKINIT et produira un TGT dans le ccache spécifié. Il affichera également la clé de chiffrement AS-REP dont vous pouvez avoir besoin pour l'outil getnthash.py.
  
  Command Reference:

      Domain: test.local

      Host that you got the certificate from: DC01

      PFX file: crt.pfx

      PFX file password: password123

      TGT requested: out.ccache

command: |
  python3 gettgtpkinit.py test.local/DC01\$ -cert-pfx crt.pfx -pfx-pass password123 out.ccache
items:
  - Username
  - Password
  - PFX
services:
  - Kerberos
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
  - PrivEsc
references:
  - https://github.com/dirkjanm/PKINITtools
  - https://dirkjanm.io/ntlm-relaying-to-ad-certificate-services/
---
