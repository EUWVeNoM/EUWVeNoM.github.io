---
description: |
  Le fichier dcomexec.py d'Impacket fournit un shell interactif sur l'hôte Windows, similaire à wmiexec.py, mais utilisant différents points d'extrémité DCOM.

  Il prend actuellement en charge les objets DCOM MMC20.Application, ShellWindows et ShellBrowserWindow.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

  	DCOM Object: MMC20
command: |
  python3 dcomexec.py -object MMC20 test.local/john:password123@10.10.10.1
items:
  - Password
  - Username
services:
  - DCOM
OS:
  - Linux
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/dcomexec.py
  - https://riccardoancarani.github.io/2020-05-10-hunting-for-impacket/
---
