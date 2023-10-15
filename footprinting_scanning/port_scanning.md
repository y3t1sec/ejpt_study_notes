PortScanning can be used to Identify Operating Systems and accessible services.
Doing this is very loud, and will lead to detection, but is allowed in a PenTest

Use footprinting, to establish services, by examining the responses from hosts, and checks against a signature database. Some OS are more obvious than others, and some services will explicitly tell us what OS this is installed on.

If the port is open:
syn > syn/ack > ack

If the port is open
syn > ack

Nmap includes a stealthy scan. (used to evade IDS)
syn > syn/ack > RST

UDP scans are slower, response open|filtered can be sped up by increasing rate (min-rate)

Nmap Automator, can run new scans and continue enumerating further, rustscan is fast and made out of rust, and autorecon which will tell you everthing you can know from scanning.
