Bandit Level 28 → Level 29 (Reading Git Logs)<br>
Level Goal<br>
There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

rm -rf repo > ıf u get error u need to delete the repo to download new one.

<img src="https://i.imgur.com/RarcxQK.png" height="70%" width="70%">

<img src="https://i.imgur.com/ni8JEA4.png" height="30%" width="30%">
We need to check info leak we need the password
<img src="https://i.imgur.com/nG2E0Ue.png" height="70%" width="70%">
Shows redacted text (git log -p)

<img src="https://i.imgur.com/KJi6kZf.png" height="70%" width="70%">

Password: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0
