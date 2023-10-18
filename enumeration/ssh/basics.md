SSH is a simple tool that allows you to remotely access devices with an encrypted connection over port 22

ssh root@

You can also use nc to connect to ssh if you specify the port. This can allow you to enumerate the version information or view the banner without connecting.

Good nmap scripts:
--script=ssh2-enum-algos (enumerate algorithms used to create key)

--script=ssh-hostkey --script-args  ssh_hostkey=full

--script=ssh-auth-methods --script-args="ssh.user=<username>" ( can help you identify accounts without creds)
