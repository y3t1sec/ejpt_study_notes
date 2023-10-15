Ports use both TCP and UDP (writing because I often forget to scan UDP)
https://linux.die.net/man/1/nmap

Useful tags
-F - fast scan
-Pn - No Ping
-sU - UDP scan
-T# - Aggressiveness of your scan 0-5, timing templates. Lower ones can be used to evade IDS.
-v# - increase verbosity v-vvvvv
-oX - Output to XML file (to input into faraday or something to keep track of your work) or metasploit.
-sC - run default scripts (loud as hell and will get you caught)
-sV - version fingerprinting
-A - Aggressive scan, combo of sC sV and O
