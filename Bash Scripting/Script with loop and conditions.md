- Script:

```#!/bin/bash

if [ "$1" == ""] 
then
echo "enter an ip address"
echo "syntax: ./ipsweep.sh 10.0.2"

else
for ip in `seq 1 254`; do 
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &       ($1 basically means arguement 1: so we run this script using command ./ipsweep.sh 10.0.2 [$0 is ./ipsweep.sh]) (& is being used here to speed up the process by allowing multiple instances of this loop to run at once.)

done 
fi
```