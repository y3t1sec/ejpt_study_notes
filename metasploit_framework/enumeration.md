For this we will be primarily utilizing auxiliary modules.

Things like port scanning are especially beneficial for pivoting from a compromised device.

note: the auxiliary/admin modules require credentials.


**modules**

search portscan 

auxiliary/scanner/portscan/tcp

search udp_sweep

auxiliary/scanner/discovery/udp_sweep

to add the route to a meterpreter session **note: for portscanning you must use scanner/portscan/tcp as db_nmap appears unreliable**

run autoroute -s <ip.addr>

**ftp enumeration**

search type:auxiliary name:ftp

auxiliary/scanner/ftp/ftp_login

**SMB**

search type:auxiliary name:smb

auxiliary/scanner/smb/smb_enumusers
auxiliary/scanner/smb/smb_enumshares
auxiliary/scanner/smb/smb_login

**webserver**

scanner/http/http_header
scanner/http/http_version
auxiliary/scanner/http/robots_txt
scanner/http/dir_scanner
auxiliary/scanner/http/files_dir
auxiliary/scanner/http/http_login
auxiliary/scanner/http/apache_userdir_enum

**MySQL**

auxiliary/scanner/mysql/mysql_version
auxiliary/scanner/mysql/mysql_login
auxiliary/admin/mysql/mysql_enum (requires creds)
auxiliary/admin/mysql/mysql_sql (reqs creds)
auxiliary/scanner/mysql/mysql_schemadump

**SSH**

auxiliary/scanner/ssh/ssh_login

**SMTP**

auxiliary/scanner/smtp/smtp_version
