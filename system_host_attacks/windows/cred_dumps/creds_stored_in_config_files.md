Windows supports the mass rollout / installation of windows. This is typically done through the use of the unattended windows setup util.

This uses configuration files that contain specific configurations and user account creds. Specifically the admin account's password. If these are left on the system after installation they can reveal user account creds that can be used by attackers to auth with windows legitimately.

C:\Windows\Panther\Unattend.xml
C:\Windows\Panther\Autounattend.xml

As a security precaution the passwords stored in this file are base64 encoded.
