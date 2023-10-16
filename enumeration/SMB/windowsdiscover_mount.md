SMB is a windows implementation of a file share.

CIFS is the generic term for it, NETBIOS used to be required for SMB, and is often used to this day (poisoning?)

nmap default SMB scripts do a lot of useful SMB enumeration.

**Good cmds to remember**

net use

smbclient

**Good Nmap Scripts**

https://nmap.org/nsedoc/scripts/smb-enum-sessions.html
https://nmap.org/nsedoc/scripts/smb-enum-shares.html
https://nmap.org/nsedoc/scripts/smb-enum-users.html
https://nmap.org/nsedoc/scripts/smb-server-stats.html
(you can run them all with --script smb*)
