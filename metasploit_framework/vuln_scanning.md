 For this we will be searching for metasploit exploit modules to run.

 db_nmap - will allow you to run and import nmap scans direct through metasploit.

 Metasploit autopwn: https://github.com/hahwul/metasploit-autopwn

 load db_autopwn after install

 Very useful module for assessing services discovered or loaded into MS.

 analyze command can be helpful to also limit the list of known vulns.

Starting Nessus: sudo systemctl status nessusd.service

When this is run it will show you the link to access. After your scan you can filter by metasploit modules. and you can export the xml to import into the metasploit database:

Click into the appropriate scan. In the top right you should see an export option. Download the Nessus file. This will download as an xml file. Then in Metasploit, use the db_import option as mentioned earlier, pointing to the Nessus xml file.

**webapps**

web app vuln scanner that can be used to enumerate and scan web apps for vulns. Available as a MSF plugin to load direct into MSF and fully integrates. You just need to load it in.

load wmap

all commands start with wmap_ so you can tab to find what you need

wmap_sites -a ip.addr

wmap_sites -t http://ip.addr

To run your scan you must run the following in order

wmap_run -t (to load all modules
wmap_run -e (to scan with all modules in profile
wmap_vulns (will list the discovered vulnerabilities)
