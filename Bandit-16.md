Bandit Level 16 → Level 17 (Nmap Enumeration)<br>
Level Goal<br>
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

nmap to see open ports

<img src="https://i.imgur.com/z1IAWfP.png" height="50%" width="50%">

Password: SSHKEY
