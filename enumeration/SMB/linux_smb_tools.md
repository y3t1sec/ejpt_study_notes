nmap --script=smb*

--script=smb-protocols
--script=smb-enum-users
trick if you have the time to just run every script

msfconsole has numerous modules to break smb
auxiliary/scanner/smb/smb2

nmblookup -A <ip address>
smbclient -L <ip address< -N

rpcclient -U "" -N <ip addr>
srvinfo
enumdomusers
lookupnames admin

https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html

enum4linux -o <ipaddr> 
enum4linux -U <ipaddr>

A good link noting all of these topics in a clear format.
