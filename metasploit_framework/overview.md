![image](https://github.com/y3t1sec/ejpt_study_notes/assets/129677280/83469ef2-e708-4127-8993-36da425e473a)

Modules are pieces of code that can be executed by the metasploit framework.

Types

exploit - a module that is used to take advantage of a vuln and is paired with a payload (typically)
payload - code that is delivered by MSF and remotely executed on the target after exploitation. ex. a reverse shell that initiates a connection from the target system back to the attacker
   - nonstaged payload - payload that is sent to the target and is along with the exploit
   - staged payload - sent to the target in two parts. The first part (stager) contains a payload that is used to establish a reverse connection to the attacker, and download the second part of the payload (stage) and execute it.
   - meterpreter - advanced multi-functional payload that is executed in memory on the target system to avoid detection. It communicates over a stager socker and provides the attacker with an interactive command interpreter on the target system that facilitate s the execution of system commands, fs navigation, keylogging and much more
encoder - used to encode payloads in order to avoid AV detection. ex. shikata_ga_nai
NOPS - used to ensure that payloads sizes are consistent and to ensure stability when executed
auxiliary - a module that is used to perform additional functionality like port scanning and enumeration (any module that cannot be paired with a payload)

file system /usr/share/metasploit-framework/


Modules are stored under /modules, and custom modules are stored under ~/.ms4/modules
