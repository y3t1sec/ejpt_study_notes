The tool used for the lab is called arpspoof.

This is a guide to using ettercap: https://itigic.com/arp-poisoning-attack-how-to-do-it-on-kali-linux/

Note: You will need to configure your kali box to forward IP packets or this will not work.

echo 1 > /proc/sys/net/ipv4/ip_forward

Command used in the lab is the following

arpspoof -i eth1 -t [ target ] -r [ target 2 route ] 

But I performed the same attack with ettercap and found it much simpler to perform. The -h for arpspoof is not very useful.
