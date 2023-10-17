msfconsole
auxiliary/scanner/smb/smb_login

pass_file"usr/share/wordlists/metsaploit/unix_passwords.txt"
smbuser

gzip -d /usr/share/wordlists/rockyou.txt.gz
hydra -l admin -P /usr/share/wordlists/rockyou.txt <targetip> <protocol>

smbmap -H <ipaddr> -u admin -p <passwd>

smbclient -L <ipaddr> -U <usrname>

smbclient //<addr>/<share> -U <username>
tar-xf

Named pipes are pipes that are known, and if we have access to SMB we may be able to get access to other services.

https://learn.microsoft.com/en-us/windows/win32/ipc/named-pipes

msfconsole

To enumerate SIDS

enum4linux -r -u "username -p "password" <ipaddr>

auxiliary/scanner/smb/pip_auditor
