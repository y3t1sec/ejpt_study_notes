nmap --script=smb*
trick if you have the time to just run every script

msfconsole has numerous modules to break smb

nmblookup -A <ip address>
smbclient -L <ip address< -N

rpclient -U "" -N <ip addr>

https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html

A good link noting all of these topics in a clear format.
