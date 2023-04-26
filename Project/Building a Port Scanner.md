```
#!/bin/python3

import sys
import socket
from datetime import datetime

#DEFINE OUR TARGET
if len(sys.argv) == 2: #first arguemwnt (here) is scanner.py and second is the ip address itself
	target= socket.gethostbyname(sys.argv[1]) #translates hostname to ipv4
else:
	print("Invalid number of arguements")
	print("correct syntax: python3 scanner.py <ip>")
	
#ADD A PRETTY BANNER
print("-"*50)
print("Scanning Target: ",target)
print("Time Started: ",datetime.now())
print("-"*50)


try:
	for port in range(1,100):
		s=socket.socket(socket.AF_INET, socket.SOCK_STREAM)
		socket.setdefaulttimeout(1)
		result=s.connect_ex((target, port)) #connect_ex is a result checker that gives 1 if error occurs and 0 for no errors.
		if result==0:
			print(f"Port {port} is open")
		s.close()
		
except KeyboardInterrupt:
	print("\nExiting Port Scanner")
	sys.exit()
	
except socket.gaierror: #when hostnames can't be resolved
	print("Hostname couldn't be resolved")
	sys.exit();
	
except socket.error:
	print("Coudln't connect to the server")
	sys.exit()


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

INPUT

python3 scanner.py 172.18.176.10

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

OUPUT

--------------------------------------------------
Scanning Target:  172.18.176.10
Time Started:  2023-02-04 05:45:39.364553
--------------------------------------------------
Port 53 is open


```