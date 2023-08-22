---
description: |
  Module PowerShell permettant d'exporter, d'importer, de supprimer, d'autoriser et de publier des modèles de certificats Active Directory. Il inclut également une ressource DSC pour créer des modèles AD CS à l'aide de ces fonctions. Ce module a été conçu dans le but d'utiliser DSC pour des constructions rapides en laboratoire, mais il pourrait également être utilisé dans des environnements de production pour déplacer des modèles entre des environnements AD CS. Cette commande est utilisée pour dupliquer un modèle AD CS existant.

  Command Reference:

    Name of new created template: <newMaus>

    Name of duplicated template: <Subordinate Certification Authority>

    Identity: <domain.local\PKI Admins>

command: |
  New-ADCSTemplate -DisplayName <newMaus> -JSON (Export-ADCSTemplate -DisplayName "<Subordinate Certification Authority>") -publish -Identity "<domain.local\PKI Admins>"

code: |
  The ADCSTemplate module contains the following PowerShell functions:

    Export-ADCSTemplate
    Get-ADCSTemplate
    New-ADCSDrive
    New-ADCSTemplate
    Remove-ADCSTemplate
    Set-ADCSTemplateACL
 
items:
  - Shell
services:
  - LDAP
  - ADCS
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
  - Exploitation
references:
  - https://github.com/GoateePFE/ADCSTemplate
---