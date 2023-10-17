File Transfer Protocol - used to store files on server and "access them remotely"

NOrmally perform a services an OS scan to look for vulns (nmap)

cmds

ftp (help will show all commands)

attempt anon login to see if you can access it anonymously

recommends hydra for bruteforcing FTP

for this lab /usr/share/metasploit-framework/data/wordlists/common_users.txt and /usr/share/metasploite-framework/data/wordlists/unix_passwords


can also bruteforce with nmap using --script=ftp-brute


**Default Bad Configs**

--script=ftp-anon

anonymous ftp login is a common issue. people intimidated by sharing creds securely or don't want to read the docs to set it up right.



