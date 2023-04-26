```
#!/bin/pyton3
import socket

HOST="127.0.0.1"
PORT=7777

s= socket.socket(socket.AF_INET, socket.SOCK_STREAM) #AF_INET is ipv4 and SOCK_STREAM is port number

s.connect((HOST,PORT)) #double parenthesis as parameter is a tuple.

```