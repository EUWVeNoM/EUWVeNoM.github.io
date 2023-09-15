---
description: |
  SharpLDAPmonitor.exe vous permet de surveiller la création, la suppression et les modifications des objets LDAP en direct pendant votre pentest.

  Command Reference:

  	Target IP: 10.10.10.1

  	Attacker IP: 10.10.10.2

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  SharpLDAPmonitor.exe /dcip:10.10.10.1 /user:TEST.local\john /pass:password123

items:
  - Password
  - Username
services:
  - LDAP
  - Kerberos
  - NTLM
OS:
  - Windows
  - Approved-tool
attack_types:
  - Enumeration
references:
  - https://github.com/p0dalirius/LDAPmonitor/tree/master/csharp
---
