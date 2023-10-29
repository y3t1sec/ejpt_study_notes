PTH involves stealing or capturing the NTLM hash or clear text password and using them to authenticate with the target. We can use multiple tools to facilitate pass the hash attacks.

 - metasploit psexec module
 - crackmap exec

This technique will allow us to ontain access to the target system.

NOTE: Metaploit module requires you to specify the LM hash and NTLM hash

exploit/windows/smb/psexec ( include the username and hashes ) ( you may need to set target to native \ upload )

