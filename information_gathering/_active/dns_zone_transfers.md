DNS is the protocol that is used to resolve domain names to IP addresses (and vice versa)
Public DNS servers (8.8.8.8, 1.1.1.1, etc) contains the domain names of nearly every clearnet site.

A cheatsheet of all the different types of DNS records: https://constellix.com/news/dns-record-types-cheat-sheet

**DNS Interrogation**
The process of enumerating DNS records for a domain. The objective is to probe a DNS server to try and provide the DNS records for the entire domain. This process can provide information like the IP address, subdomains,MX records, SPF records (often containing site IPs)

**DNS Zone Transfer**
https://digi.ninja/projects/zonetransferme.php
If an admin wants to copy or transfer zone files from one server to the other they will leave this open. If this is misconfigured, an attacker can copy the zone to a server they control. This can provide pen testers or attackers with a holistic view of the organization.
Zone Transfers can be performed with dig.

dig axfr @<ns.domain.com> <domain.com>

Without or before DNS servers all changes were being done with the hosts file. 

Included in Kali is the command **dnsenum**. This can be used to enumerate subdomains
**Note** This will bruteforce by default.

A tool like fierce can be used for DNS bruteforce. Along with sublist3r, dnsrecon, gobuster, ffuf, etc
https://github.com/mschwager/fierce
