---
description: |
  Evil-WinRM utilise l'instrumentation de gestion Windows (WMI) pour vous donner un shell interactif sur l'hôte Windows. Winrm supporte PKINIT, ce qui signifie que si vous avez un fichier PFX d'ordinateur, vous pouvez vous authentifier et obtenir un shell. Notez que la commande nécessite une clé publique et une clé privée au format PEM, qui peuvent être extraites en convertissant le PFX au format PEM. Consultez les références pour plus d'informations à ce sujet. Les fichiers PFX protégés par un mot de passe peuvent être craqués avec JohnTheRipper.

  Command Reference:

  	Target IP: 10.10.10.1

  	PFX File: cert.pfx

  	Domain: EVILCORP

command: |
  evil-winrm -i 10.10.10.1 -c pub.pem -k priv.pem -S -r EVILCORP

code: |
  openssl pkcs12 -in certificate.pfx -out certificate.pem -clcerts

items:
  - PFX
services:
  - WMI
OS:
  - Windows
  - Approved-tool
attack_types:
  - Exploitation
references:
  - https://github.com/Hackplayers/evil-winrm
  - https://book.hacktricks.xyz/cryptography/certificates
---
