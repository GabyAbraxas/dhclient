How to Use the Script
Save the script to a file named dhclient2.py.

Make the script executable (optional):

bash
Copy code
chmod +x dhclient2.py
Run the script with the following commands:

To release and renew the IP:
bash
Copy code
python dhclient2.py -r eth0
To renew the IP without releasing:
bash
Copy code
python dhclient2.py eth0
Example Outputs
Obtaining a New IP:
plaintext
Copy code
Current IP for eth0: 192.168.1.10
Renewed IP for eth0.
New IP for eth0: 192.168.1.20
Summary: Previous IP: 192.168.1.10, New IP: 192.168.1.20
Releasing and Obtaining a New IP:
plaintext
Copy code
Current IP for eth0: 192.168.1.10
Released IP for eth0.
Renewed IP for eth0.
New IP for eth0: 192.168.1.25
Summary: Previous IP: 192.168.1.10, New IP: 192.168.1.25
Notes:
Permissions:

The script uses sudo for commands like dhclient and dhclient -r. Make sure the user running the script has sufficient privileges.
Dependencies:

Ensure the ip and dhclient commands are installed and accessible.
Error Handling:

The script includes basic error handling for cases like missing interfaces or command failures.
