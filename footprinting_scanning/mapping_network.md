Scope and Discovery

When you start a penetration test you're going to have to negotiate the scope. Determine what is the most use, what would provide them with the most use and value.
He is stating that some clients might just want a box ticked for their audit, but to be cautious of taking down a production system leading to loss of income or loss of life.
Part of this is to determine how much access you will have to start, but some clients will have a "come at me bro" response which can be harder to provide them something useful.

We will be going through the process:
physical access
sniffing
arp
ICMP

**Physical Access**
Physical security - in some cases this may be required to confirm the physical security of the customer
OSINT - Open Source Intelligence, using DNS records and websites to find IP addresses and entry points
Social Engineering - Could you get someone to tell you whatever you need or provide you access

**Sniffing**
Passive Reconnaissance - Through sniffing hte network we can discover what is available, possibly find hashes on insecure protocols, etc
Watch Network Traffic to determine normal use

**ARP**
Maps IP addresses to MAC addresses, this is a legacy broadcast protocol that to listen to the traffic happening on the network. Using an ARP scan you can hear everything physically connected to the network. In some cases this may be disabled, and everything would be added to ARP tables

**ICMP**
Used to determine Internet connectivity issues, ping and tracroute both use this protocol
This is called an echo request, like a RADAR system. Sometimes this is disabled to prevent ping scans

**Tools**

WireShark - Can be used to listen to packets and network traffic. From here you can save a PCAP, and filter (statistics > endpoints)

ARP-SCAN - can be used to sweep ARP broadcasts to listen to discover what is connected (can use MAC to determine device type)

Ping - will let you know if the device is online using ICMP requests will also inform you of the latency which can tell you location

FPing - similar to ping, but can be sent to multiple hosts at one time (you can filter out errors with 2>/dev/null)

Nmap - available on all OS, learned about in active recon chapter 

ZenMap - zenmap is nmap, but with a GUI, it's opensource and free, and available on all OS
zmap - not discussed in this video, but zmap is a version of nmap, with slightly less functionality, but can run faster.
