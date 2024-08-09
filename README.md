cakes = {"small":3,"medium":4,"large":5}
icecreams = {"small":1,"medium":2,"large":3}
icecreamcake = {"small":4,"medium":6,"large":8 }
toppings = {"chocolate":1,"marshmallows":1,"sprinkles":1,"candies":1}
flavors = {"vanilla":1,"strawberry":1,"chocolate":1}
checkout=["Order completed for "]
#cakesMap = {"s":3,"m":4,"l":5}


def order(user_name,index):
   order = input('What would you like to order cake, icecream or icecream cake? \n')

   if order == 'icecream':
     return icecream(user_name, index)
   if order == 'cake':
     return cake(user_name, index)
   if order == 'icecream cake':
     return ice_cream_cake(user_name, index)
   else:
      cost+=0

"""def cake(user_name):
   quantity = int(input("How many cakes do you want?\n"))
   cost = int(0)
   size = input("What size do you want?(use s,m,l accordingly)\n")
   cost+=cakesMap.get(size)"""
   

def cake(user_name, index):
   quantity = int(input("How many cakes do you want?\n"))
   cost = int(0)
   size = input("What size do you want?(use s,m,l accordingly)\n")
   if size == 's':
      cost+=cakes.get("small")
   if size == 'm':
      cost+=cakes.get("medium")
   if size == 'l':
      cost+=cakes.get("large")
   else:
      cost+=0

   flavor = input("What flavor would you like?\n")
   if flavor == 'vanilla':
      cost+=flavors.get("vanilla")
   if flavor == 'strawberry':
      cost+=flavors.get("strawberry")
   if flavor == 'chocolate':
      cost+=flavors.get("chocolate")
   else:
      cost+=0

   topping = input("What topping do you want?\n")
   if topping == 'chocolate':
      cost+=toppings.get("chocolate")
   if topping == 'marshmallows':
      cost+=toppings.get("marshmallows")
   if topping == 'sprinkles':
      cost+=toppings.get("sprinkles")
   if topping == 'candies':
      cost+=toppings.get("candies")
   else:
      cost+=0
  
   if quantity > 1:
      quantitycost = int(0)
      for i in range(quantity):
         quantitycost += cost

         
   checkout.append(user_name)
   print("Your per order cost is $ " + str(quantitycost))
   print(checkout[0] + checkout[index]+"\n")

   return quantitycost


def icecream(user_name, index):
   quantity = int(input("How many icecreams do you want?\n"))
   cost = int(0)
   size = input("What size do you want?\n")
   if size == 's':
      cost+=icecreams.get("small")
   if size == 'm':
      cost+=icecreams.get("medium")
   if size == 'l':
      cost+=icecreams.get("large")
   else:
      cost+=0

   flavor = input("What flavor would you like?\n")
   if flavor == 'vanilla':
      cost+=flavors.get("vanilla")
   if flavor == 'strawberry':
      cost+=flavors.get("strawberry")
   if flavor == 'chocolate':
      cost+=flavors.get("chocolate")
   else:
      cost+=0

   topping = input("What topping do you want?\n")
   if topping == 'chocolate':
      cost+=toppings.get("chocolate")
   if topping == 'marshmallows':
      cost+=toppings.get("marshmallows")
   if topping == 'sprinkles':
      cost+=toppings.get("sprinkles")
   if topping == 'candies':
      cost+=toppings.get("candies")
   else:
      cost+=0

   if quantity > 1:
         quantitycost = int(0)
         for i in range(quantity):
            quantitycost += cost
            
   checkout.append(user_name)
   print("Your per order cost is $ " + str(quantitycost))
   print(checkout[0] + checkout[index]+"\n")

   return quantitycost



def ice_cream_cake(user_name, index):
   quantity = int(input("How many icecreamcakes do you want?\n"))
   cost = int(0)
   size = input("What size do you want?\n")
   if size == 's':
      cost+= icecreamcake.get("small")
   if size == 'm':
      cost+=icecreamcake.get("medium")
   if size == 'l':
      cost+=icecreamcake.get("large")
   else:
      cost+=0
   
   flavor = input("What flavor would you like?\n")
   if flavor == 'vanilla':
      cost+=flavors.get("vanilla")
   if flavor == 'strawberry':
      cost+=flavors.get("strawberry")
   if flavor == 'chocolate':
      cost+=flavors.get("chocolate")
   else:
      cost+=0

   topping = input("What topping do you want?\n")
   if topping == 'chocolate':
      cost+=toppings.get("chocolate")
   if topping == 'marshmallows':
      cost+=toppings.get("marshmallows")
   if topping == 'sprinkles':
      cost+=toppings.get("sprinkles")
   if topping == 'candies':
      cost+=toppings.get("candies")
   else:
      cost+=0


   if quantity > 1:
         quantitycost = int(0)
         for i in range(quantity):
            quantitycost += cost
            
   checkout.append(user_name)
   print("Your per order cost is $ " + str(quantitycost))
   print(checkout[0] + checkout[index]+"\n")

   return quantitycost



def donate(quantitycost):
   newcost = quantitycost+1
   print("Your new total is: $" + str(newcost))
   return newcost

orders = int(input("how orders do you want to place?\n"))
cost=int(0)
for i in range(orders):
   user_name = input("Enter your name for Order #: " +str(i+1)+ "\n")
   cost+= int(order(user_name, i+1))


      
donation = input("Would you like to donate $1?\n")
if donation =='yes':
   donate(cost)
else:
   print("Total orders cost $" + str(cost))




print("Thanks For Shopping With Us!")
