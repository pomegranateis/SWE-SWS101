# Exploiting VNC 

The command nmap -sV 10.40.1.118 -p 5900 revealed that port 5900 was open and running the VNC service.

The vnc_login exploit was chosen for its effectiveness in gaining unauthorized access to the target system.

I encountered issues where changing the VNC server password did not affect the default port (5900), indicating a potential vulnerability in the password change mechanism.

The complexity of configuring and securing VNC servers, especially when dealing with multiple ports or different versions of the VNC service.

importance of securing remote access services