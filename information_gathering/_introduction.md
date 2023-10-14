Alexis Ahmed is the primary instructor for this portion of the course. Recognized from the HackerSploit channel.

Passive and Active Information Gathering. Reconnaissance is used interchangably with Information Gathering.

Once you learn the difference between the two, they will walk you through using the tools associated with passive and active information gathering.

##Passive Information Gathering
Using online resources to learn about your target, publicly accessible information.(OSINT)
Gather as much information as possible without engaging the target.
You could interact with the website as a regular end user, and learn about some of the technologies and permissions of the app.
Identifying IP addresses and DNS information
Identify domain names and domain ownership information
Identify email addresses and social media profiles (correlate)
Identify web technologies being used
Identify subdomains (without hitting)

##Active Information Gathering
Interacting with the target to learn mmore about it. Fingerprinting and actively engaging with the target.
Performing tests against what you have learned about the test.
Shaking the hand with the target.
Actually interacting with the target, this means that you will need to retreive permission before you interact as this could be considered illegal.
Discovering open ports on target
Learn about the internal infrastructure of the target network / org
Enumerate information from the target systems


##Prereqs
Basic Familiarity with Linux (Met)
Basic familiarity with Web Technologies (Protocols, TCP/IP, HTTP, etc)(Met)

**Disclaimer**
Never run these TTPs without proper authorization. Without written authorization it is safe to assume that you are breaking the law.

This is the first phase of any penetration test. It involved gathering or collecting information about the commpany or individual or website you have been asked to target. Oftentimes, the more information you collect on the target, the more successful you will be.

You will want to identify what technologies are being used, if they have any known vulnerabilities. IP addresses and domains utilized by the target. You can make this as wide or as narrow as the scope of the penetration test requires.
You can either learn about the technologies at play to determine the foothold, or you can learn about the employees, their emails, etc. This comes in handy in later in the test as you can pivot to performing a phishing test based on the intel you gathered in the earlier phases of the test. Additionally, you can determine the best next step to pivot.

If I want to compare this to a HTB machine. All I am provided is an IP address, but as I dive deeper, and perform more recon I am able to learn about the box, and determine my next steps from there.

