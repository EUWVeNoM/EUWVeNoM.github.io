---
description: |
  Pour monter un partage SMB (Server Message Block) à l'aide de la commande mount sous Linux, vous utilisez généralement le type de système de fichiers cifs, qui est une implémentation du protocole SMB.

  Command Reference:

    Username: Guest

    password: empty

    Share: //10.129.253.46/Development

    Local folder: devel

command: |
  mount -t cifs -o vers=2.1,username='Guest',password='' //10.129.253.46/Development devel

items:
  - No_creds
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://www.chrisrmiller.com/mount-samba-share-in-ubuntu/
  - https://askubuntu.com/questions/1050460/how-to-mount-smb-share-on-ubuntu-18-04
---