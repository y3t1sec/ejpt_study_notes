Server Message Block is a network file sharing protocol and is used to share files and peripherals ( printers serial ports USB ) between computers on a LAN.

SMB uses ports 445 (TCP ) and 139 (NETBIOS)

Samba is the OSS Linux implementation that allows windows systems to access linux shares and devices.

SMB has 2 levels of auth ( user and share authentication )

 - user : users must prove a username and pw to auth with SMB server
 - share : users must provide pw to access restricted share

        > auth req >
CLIENT  < encrypt string with user's hash <   SERVER
        > encrypted string >
        < access granted <

PSEXEC is a telnet replacement (from MS ) that allows you to execute process on remote windows computers using any users creds

Auths via SMB

We can use psexec to auth with target ( have to steal credentials to use )

Similar to RDP but there is no GUI

For brute forcing you can use enumeration or common user accoutns ( Administrator , Guest )

**Exploitation**

nmap scan ( probably want to use service versioning )

auxiliary/scanner/smb/smb_login

exploit/windows/smb/psexec ( note : this will trigger antivirus on most systems in the wild )

psexec.py < username >@ip.addr cmd.exe

**MS17-010**

Name given to a collection of exploits was leaked to the public by a group of civilians.

Was also used in the WannaCry ransomware group and impacts multiple versions of windows (windows vista through windows 10)

Microsoft released a patch in March 2017, but it is still viable as thousands of servers are still exploitable.

Toolset to crack: https://github.com/3ndG4me/AutoBlue-MS17-010

Read the docs. Start with shell_prep.sh




