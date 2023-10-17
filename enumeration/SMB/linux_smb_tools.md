nmap --script=smb*

--script=smb-protocols

--script=smb-enum-users

--script=smb-enum-shares

trick if you have the time to just run every script

msfconsole has numerous modules to break smb
auxiliary/scanner/smb/smb2
auxiliary/scanner/smb/smb_enumshares


nmblookup -A <ip address>
smbclient -L <ip address> -N
smbclient //<ipaddr>/<shares> -N

rpcclient -U "" -N <ip addr>
srvinfo
enumdomusers
lookupnames admin
enumdomgroups


https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html

https://www.kali.org/tools/enum4linux/
enum4linux -o <ipaddr> 
enum4linux -U <ipaddr>
enum4linux -S <ipaddr>
enum4linux -G <ipaddr>
enum4linux -i <ipaddr>

A good link noting all of these topics in a clear format.
