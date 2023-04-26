`ls -al`
`chmod +rwx hello.txt`
`chmod 755 hello.txt` read=4; write=2; execute=1
`sudo adduser <username>`
`sudo cat /etc/shadow` displays the hashes of passwords of all users.
`sudo cat /etc/sudoers` displays what members have what prviliges.
`grep 'sudo' /etc/group` to check what memebers have sudo perms
`ip a` new substitute of ifconfig
`iwconfig` to view wireless connections
`ip n` n stands for neighbour (alternate command > arp -a): checks for what ip is associated to what mac 
`ip r` alternate > route : to view routing table
`systemctl enable <service name>` (ex: systemctl enable ssh)
`python -m http.server <port number> (80)` to start a web server





