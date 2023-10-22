Mostly exploiting the inherent weaknesses in windows and linux.

Will be discussing the various services running in Linux and windows. They will mostly be talking about how to esclate priveleges in windows (kernal exploits, etc) windows filesystem vulns (alternate data streams) Windows credential dumping (plaintext from memory, and NTLM hashes) and how those move to lateral movement.

Then we will be discussing Linux (ssh, samba, etc) privelege escalation (SUID binaries cron jobs, etc) filesystem vulns, then credential dumping (hashes or plaintext)

These will be inherent vulnerabilities, not additional softwares that may be installed overtop.

**System / Host Based Attacks**

An attack targeted towards a specific system running a specific operating system.

More than network services are the attack vector.

Normally come into play after you have gained a foothold to a system and the further exploits that are required to acheive your objectives or root the machine.

Normally internal hosts, not externally facing.

Primarily focused on exploiting vulnerabilities or common misconfigurations in the operating system.
