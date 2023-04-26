```
#!/bin/python3
print("hello world")

#-----------------------------------------------------------------------------------------------------------------------------------------

def bio():
	name= "indrajith"
	age= 31.9
	height= 178
	print("hello world".title())
	print("Hi I'm", name, "of age", age, "and height", height)

bio()

#-----------------------------------------------------------------------------------------------------------------------------------------

test_not= not True
print(test_not)

#-----------------------------------------------------------------------------------------------------------------------------------------

arr= ["hello", "im", 24, "years", "old"]
print(arr)
print(arr[2])
arr[1]="I am"
print(arr)

#-----------------------------------------------------------------------------------------------------------------------------------------

tup=("hello", "im", 24, "years", "old")
print(tup)

for i in tup:
	print(i)

#-----------------------------------------------------------------------------------------------------------------------------------------

line= "this line is straight"
line_split= line.split()
line_join=' '.join(line_split)
print(line_join)

name= "blackbody"
print(f"My nane is {name}.")

#-----------------------------------------------------------------------------------------------------------------------------------------

dict= {"career" : ["cyber", "defense", "business"], "skills" : ("hacking", "english"), "sport" : "football"}
print(dict)

dict["tech"]= "phone"
print(dict)

dict.update({"sport" : "F1"})
print(dict)

print(dict.get("sport"))
print(dict["sport"])


dict.update({"sport" : "football"})
print(dict)
```