```
#!/bin/python3

from shoes import shoes

cheap= shoes("Nivea", 300)
medium= shoes("Nike", 1000)
luxury= shoes("UnderArmour", 4000)

try:
	shoe_budget= float(input("Enter your shoe budget :"))
except ValueError:
	print("please specify a number for shoe budget")
	exit()
 
for i in [luxury, medium, cheap]:  # we've to go from luxury shoes to cheap shoes else its going to keep returning cheap fro everything
	i.purchase(shoe_budget)  #we already made a purchase method in our class, so this method will take care of all mentioned functions in it.


```