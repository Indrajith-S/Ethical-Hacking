
- Let's say we have an ip address: 192.168.1.26/24

- The /24 here denotes the subnet mask here or the number of existing subnets.
- As we know an IPv4 address consists of 32 bits and is divided into 4 octets of 8 bits and is represnted below:
	- 11111111.11111111.11111111.1111111: this basically denotes netmask 255.255.255.255 or in layman's terms /32 subnet mask as there are 32 1's.

- now let's say there's an ip address: 192.168.1.0/23:
	- 11111111.11111111.11111110.00000000
		- this denotes netmask 255.255.(128+64+32+16+8+4+2=254).0
	
	- Now here as the calculations are being dealt in the third octet we use this format: 255.255.x.0, hence we get this subnet range:
		- 192.168.1.1 to 192.168.2.254 where 192.168.1.0 and 192.168.2.255 are network and broadcast addresses respectively giving us a total of 512 addresses where 510 are hosts or usable addresses.
		- We get this number by doing simple math. So as we can see above, we have 9 remaining zeros in /23 subnet case, hence we do 2^9 which gives us 512.


- Now let's say we have 192.168.5.0/21: 255.255.(128+64+32+16+8=248).0, which gives us 11 zeros, hence 2^11= 2048.
	- So we'll have 192.168.5.0 to 192.168.13.255 with a total of 2048 addresses where 2046(255+256+256+256+256+256+256+255) are hosts or usable addresses.

- Go to ipaddressguide.com to cross check our CIDR(classless inter-domain routing) noation.
- The bigger the subnet mask, the lesser the size of the subnet or smaller the network size.