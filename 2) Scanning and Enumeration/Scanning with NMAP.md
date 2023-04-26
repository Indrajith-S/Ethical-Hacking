- Now performing an arp-scan to enumerate the ip address of kioptrix machine by discovering all active hosts in the network
- We can use commands of two tools for the above mentioned: 
	`arp-scan -l` 
	`sudo netdiscover -r <ip subnet> (192.168.146.0/24)``


- Using NMAP:
	`nmap -T4 -p- -A` 
	(T4 stands for speed, i.e, 1 being the slowest and 5 being the fastest; -p- scans top 1000 ports; -A stands for agressive scan, that is scans for everything like version detection, OS  detection, traceroute , fingerprinting, etc)

- Using Nikto
	`nikto -h http://192.168.146.129 (-h stands for host)`