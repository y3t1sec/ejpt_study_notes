With Linux, you cannot authenticate with the hashes like you can with Windows. You will need to crack them.

All password hashes are stored in /etc/shadow but you will require elevated priveleges to review.

Use this to read the file: https://www.cyberciti.biz/faq/understanding-etcshadow-file/

Metasploit:

post/linux/gather/hashdump

auxiliary/analyze/crack_linux
