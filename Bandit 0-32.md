#  OverTheWire

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.



Bandit Level 0 → Level 1 (Reading File)
Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.



Password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

exit

Next Challange: SSH bandit1@bandit.labs.overthewire.org -p 2220
Password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

Bandit Level 1 → Level 2 (Reading File with Special Characters)
Level Goal
The password for the next level is stored in a file called - located in the home directory



Password: PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

Bandit Level 2 → Level 3 (Spaces in Filenames)
Level Goal
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory



Password: 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME


Bandit Level 3 → Level 4 (Locating Hidden Files)
Level Goal
The password for the next level is stored in a hidden file in the inhere directory.



Password: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

Bandit Level 4 → Level 5 (Linux File Command)
Level Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.



Password: 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

Bandit Level 5 → Level 6 (Linux Find Command - By Size)
Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable



Password: pXa26xhMWaC2SvDotA4r9EgZkulOeSBW


Bandit Level 6 → Level 7 (Linux Find Command - By Owner)
Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size





Password: Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3

Bandit Level 7 → Level 8 (Linux Grep Command)
Level Goal
The password for the next level is stored in the file data.txt next to the word millionth

strings - print the sequences of printable characters in files




Password: VR1ljMayciFxbnUokuQmJFw6QC9VKtub

Bandit Level 8 → Level 9 (Linux Command Piping and Sort Command)
Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

sort - Display sorted concatenation of all FILE(s).
uniq - Report or omit repeated lines. [-c|--count] , [-u|--unique]



uniq [-c|--count]:




uniq [-u|--unique]:



Password: EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

Bandit Level 9 → Level 10 (Linux Strings Command)
Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.


Password: B0s2khmbT9u0geKuOoVGW3JZKhndE3BG

Bandit Level 10 → Level 11 (Base64 Encoding in Linux)
Level Goal
The password for the next level is stored in the file data.txt, which contains base64 encoded data


CyberChef:




Password: pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro

Bandit Level 11 → Level 12 (ROT13 Encryption)
Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

ROT 13 Cipher to Decyption Tr Command (tr "A-Za-z" "N-ZA-Mn-za-m")



Password: GROozWPO8QyN0mGrjUkID0WCYkZiQxrN

Bandit Level 12 → Level 13 (Accessing Compressed Files - Gzip, Tar, Bzip2)
Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

XXD Command for Hex Dump file (xxd -r data.txt > data)



Compressed File





Password: qQYQiHOBPR8zR61qxYqX45quvihF2uzk

Bandit Level 13 → Level 14 (SSH Private Keys)
Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.
If you need help with this level: a hint file can be found in the home directory.
Make sure to read the error messages as they are informative.

SSH Private Key ( -rw—---- )





Enter Bandit13 Password Downloads SSHKEY.PRİVATE





Password: aaWecNkG4FhxJQxz07uiwzVP6bJiYS65

Bandit Level 14 → Level 15 (Netcat and Local Services)
Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

nc — arbitrary TCP and UDP connections and listens



Password: pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7

Bandit Level 15 → Level 16 (OpenSSL Encryption)
Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

ncat is a feature-packed networking utility from the Nmap Project used to read, write, redirect, and encrypt data across networks from the command line.




Password: kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

Bandit Level 16 → Level 17 (Nmap Enumeration)
Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

nmap to see open ports



Password: SSHKEY

Bandit Level 17 → Level 18 (Linux Diff Command)
Level Goal
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

1st create sshkey (Bandit16 SSHKey)


Permissions 0644 error ı need to use chmod to give permission



 diff - compare files line by line



Line:z7vPc….. (old) changed to Line:OQxX…. (new)

Password: OQxXZjELndr90zuhOTDYBEomI0SZITXI

Bandit Level 18 → Level 19 (SSH Login Commands)
Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.



Password: KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI

Bandit Level 19 → Level 20 (SUID Binary Hacking)
Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

We cant access the bandit20 file because we r user:bandit19 because of that we need to bypass bandit20



Password: 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA

Bandit Level 20 → Level 21(Netcat Port Connections)
Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

We need to Broadcast Bandit20 Password so we can get the Bandit21 Password.



Password: bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY


Bandit Level 21 → Level 22 (Linux Cronjobs)
Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

We need to access Cron.d

***** > Month,Week,Day,Hr,Min



Password: RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz

Bandit Level 22 → Level 23 (Linux Cronjobs)
Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

md5 : Hashing




Password: gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw

Bandit Level 23 → Level 24 (Linux Cronjobs)
Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

Cronjob echo "Executing and deleting all scripts in /var/spool/$myname/foo:" because of that we can change it



cat Bandit24 Passwod and directed to file ı created and ı give full file permission (chmod 777). Output that /var/spool/ and give execute permission
 


Password: hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv

Bandit Level 24 → Level 25 (Bash Scripting)
Level Goal
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time



for i in {0000..9999}; do echo “hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv $i”; done | nc localhost 30002  takes to long 

python automation 

#!/usr/bin/env python3
import socket
import sys

def brute_force():
    password = "hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv"
    
    for pincode in range(0, 10000):
        try:
            # Create NEW connection for each attempt
            with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
                s.settimeout(2)  # 2-second timeout
                s.connect(("127.0.0.1", 30002))
                
                # Read welcome message (optional)
                welcome_msg = s.recv(2048).decode()
                print(f"Trying {pincode:04d}", end='\r', flush=True)
                
                # Send attempt
                message = f"{password} {pincode:04d}\n"
                s.sendall(message.encode())
                
                # Get response
                response = s.recv(1024).decode()
                
                if "Wrong" not in response:
                    print(f"\nSuccess! PIN: {pincode:04d}")
                    print("Response:", response)
                    return True
                    
        except socket.timeout:
            print(f"\nTimeout on PIN {pincode:04d}, retrying...")
            continue
        except Exception as e:
            print(f"\nError on PIN {pincode:04d}: {str(e)}")
            continue
    
    return False

if __name__ == "__main__":
    if brute_force():
        sys.exit(0)
    else:
        print("\nFailed to find correct PIN")
        sys.exit(1)



Password: SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P

Bandit Level 25 → Level 26 (SSH Private Keys)
Level Goal
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

NOTE: if you’re a Windows user and typically use Powershell to ssh into bandit: Powershell is known to cause issues with the intended solution to this level. You should use command prompt instead.



Download SSHKey



Login Bandit26 with SSHKey


Password: SSHKey

Bandit Level 26 → Level 27 (Linux More Shell Escape)
Level Goal
Good job getting a shell! Now hurry and grab the password for bandit27!

When we login system kick us out so ı checked why that happens.



Make ur Terminal so little to enter Vim mode





After :shell cmd u will login as Bandit26



Password: STJLJBRRphMxKB392CT4iOr5CbzPU9ER


Bandit Level 27 → Level 28 (Git Readme Files)
Level Goal
There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.




Password: y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ


Bandit Level 28 → Level 29 (Reading Git Logs)
Level Goal
There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

rm -rf repo > ı need to delete the repo to download next one got error.





Shows redacted text (git log -p)



Password: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0

Bandit Level 29 → Level 30 (Viewing Git Branches)
Level Goal
There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.



We can change our Branch (git checkout dev)



Password: jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX

Bandit Level 30 → Level 31 (Git Tags)
Level Goal
There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.

Dont forget to rm old repo directory (rm -rf repo)





Password: 82NkymblpGBYmIXG6ZQ8YldBYstHpfUf

Bandit Level 31 → Level 32 (Git Commit and Push)
Level Goal
There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.

From your local machine (not the OverTheWire machine!), clone the repository and find the password for the next level. This needs git installed locally on your machine.








Password: pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT

Bandit Level 32 → Level 33 (Shell Escape)
Level Goal
After all this git stuff, it’s time for another escape. Good luck!



Shell changes every cmd to Uppercase because of that cmd doesnt work



$0 to open new Shell so Uppercase problem doesnt bother us




Password: u4P2CyPOwPGLe94RdD9Uo2FxFwvnFswM






