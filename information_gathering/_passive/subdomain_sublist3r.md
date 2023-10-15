Subdomain Enumeration (not bruteforcing)

Sublist3r uses OSINT from search engines to find subdomains, meaning that this falls under passive recon.
https://github.com/aboul3la/Sublist3r

subbrute (-b) was integrated with Sublist3r to increase the possibility of finding more subdomains using bruteforce with an improved wordlist.
Use of Subbrute falls under active reconnaissance, and can be considered active recon.

Comes in the kali repos
**Note** This tool will exceed Google's rate-limiting, causing your IP to be flagged. Best run over Tor or VPN.
-o will output the results to a txt file.
-e will specify specific search engines
