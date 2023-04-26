```
#!/bin/python3

class shoes:
	def __init__(self, name, price):
		self.name= name
		self.price= float(price)
		
	def budget_check(self, budget):  #checking if entry is valid or not
		if not isinstance(budget, (int, float)):
		 #if data type is not what is specified here then entry becomes invalid and app closes
			print("Invalid Entry! PLease enter a number")
			exit()
			
	def balance(self, budget):
		balance= budget-self.price
		return balance
		
	def purchase(self, budget):
		self.budget_check(budget)
		
		if (budget>=self.price):
			print(f"Yay! you're getting {self.name} today!")
			
			if (budget==self.price):
				print(f"You have exaclty what you need to buy {self.name}")
			else:
				print(f"Thank you for your purchase. Here's your balance ${self.balance(budget)}")
				
			exit("Thank you for using shoe budget app")

```