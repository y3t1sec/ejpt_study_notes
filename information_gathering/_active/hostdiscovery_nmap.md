Nmap can be used to discover all of the devices on the network with a pingsweep.

-sn can be used for a pingsweep, not a portscan or script scan. You have to use CIDR notation or the IP range (192.168.1.0/24 or 192.168.0.-254)

They also discuss the use of netdiscover. Netdiscover is similar, but works by sending ARP broadcasts. This might be useful for finding devices that do not show up in nmap.

