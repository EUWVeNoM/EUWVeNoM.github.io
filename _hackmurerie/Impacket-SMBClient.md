---
description: |
  Impacket's smbclient.py est un client smb générique, qui vous permet de lister les partages et les fichiers, de renommer, d'uploader et de télécharger des fichiers et de créer et de supprimer des répertoires.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  python3 smbclient.py test.local/john:password123@10.10.10.1
items:
  - Password
  - Username
services:
  - SMB
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/smbclient.py
  - https://www.hackingarticles.in/impacket-guide-smb-msrpc/
---
