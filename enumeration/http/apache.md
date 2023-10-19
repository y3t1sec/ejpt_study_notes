Largely seems very similar externally, until you get your RCE

Nmap -sV scan should inform you if you're looking at IIS or Apache

useful scripts 

--script=banner (pulls http server banner info)

Can also use MetaSploit there are a lot of useful axiliary scanner http modules

such ass 

auxiliary/scanner/http/http_version

auxiliary/scanner/http/brute_dirs ( dirb alt)

you can also curl the page, if it is too much information you can | more

You can also use wget for specific files

browsh --startup-url http://site.name (Ctrl+W exits)

lynx http://site.name also works in scenarios when you don't have a gui



