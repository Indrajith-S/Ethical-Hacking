```
#!/bin/python3

f=open("read.txt", "r")
op=f.readline(4)
print(op)
f.seek(0) # to go back to the very first line of the file
op=f.readline(2)
print(op)
f.seek(0)


for i in f:
	print(i.strip())
	
f.close()

----------------------------------------------------------------------------------------------------------

ff=open("write.txt", "a")
ff.writelines("\nLmao")


ff.close()

```