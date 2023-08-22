---
description: |
  Certipy est un outil offensif permettant d'énumérer et d'abuser des services de certificats Active Directory (AD CS). La commande find est utile pour énumérer les modèles de certificats AD CS, les autorités de certification et d'autres configurations.

  Command Reference:

    Target IP: <IP>

  	Username: <user>

  	Password: <passwd>
    
command: |
  certipy find -u <user> -p <passwd> -dc-ip <IP>

code: |
    Check following properties in templates, makes them vulnerable for ESC1.

    Client Authentication               : True
    Enrollment Agent                    : True
    Any Purpose                         : True
    Enrollee Supplies Subject           : True
    Certificate Name Flag               : EnrolleeSuppliesSubject

items:
  - Username
  - Password
services:
  - ADCS
  - LDAP
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/ly4k/Certipy
---