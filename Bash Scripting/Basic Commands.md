- Creating a ping sweep script that returns only the ip addresses of the active hosts- 

	`ping 10.0.2.1 -c 1 > ipping.txt`
	`cat ipping.txt | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" `
	 cut command cuts the specified string; 
	 -d is the delimiter where you specify a single character; 
	 -f is field: here the cut command ensures that it cuts and gives you the characters to the specified delimiter from the last known delimter
	 tr is translate or delete; 
	 -d is the character to be deleted, 
	 ":" is deleting colon

- example: 
	`cut -d "1" -f 4 for the following string: 64 bytes from 10.0.2.1: icmp_seq=1 ttl=255 time=0.241 ms`
	the output would be ttl=255 time=0.24: so as we observe above the last known delimiter was in "seq=1" (3rd) where it was cut and it cuts till the specified delimiter, i.e, 4, which is "0.241", hence our output.
