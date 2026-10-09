Bandit Level 20 → Level 21(Netcat Port Connections)<br>
Level Goal<br>
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

We need to Broadcast Bandit20 Password so we can get the Bandit21 Password.

<img src="https://i.imgur.com/DJZr7sA.png" height="70%" width="70%">

Password: bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY
