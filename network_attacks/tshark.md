Links:

https://www.wireshark.org/docs/man-pages/tshark.html

https://cheatography.com/mbwalker/cheat-sheets/tshark-wireshark-command-line/

Requires sudo or root to run a capture.

tshark -r HTTP_traffic.pcap -z io,phs -q

The above command will list how many frames are of different types. Wasn't obvious enough to me when reading the man pages so I put here as a note in case this comes up again in the future. Although I would likely use wireshark for this if given the choice.
