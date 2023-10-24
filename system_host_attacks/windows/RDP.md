Proprietary GUI remote access protocol, and uses 3389 by default. However, sysadmins often change this port to obfuscate this service.

RDP does require a valid account, so bruteforcing is a common technique.

**Exploiting RDP**

Metasploit

auxiliary/scanner/rdp/rdp_scanner ( helps you identify RDP when running on obfuscated port )

hydra to crack

hydra -l user -p password rdp://ip.addr -s port

xfreerdp /u:username /p:password /v:ip.addr

**BlueKeep** CVE-2019-0708

Released publicly by MS in 2019. Allows attackers to gain access to a chunck on kernal memory allowing them to remotely execute arbitrary code running at system level priveleges.

Impacts multiple versions of windows from XP to Server 2008 R2. There are multiple illegitimate PoCs. It is recommended to only utilize verified exploit code and modules for exploitation. There is a metasploit module to scan and to exploit the vuln.

**NOTE : attempting this specific exploit can lead to a system crash if memory is malformed**

from MSFconsole you can search bluekeep to find both relevant modules.






