# Cake & Ice Cream Ordering System 🍰🍦

Welcome to the **Cake & Ice Cream Ordering System**! This program allows users to place orders for cakes, ice creams, and ice cream cakes, with customization options like size, flavor, and toppings. The system also lets customers donate a dollar to a good cause with their order.

## Features ✨
- **Customizable Orders**: Choose from cakes, ice creams, or ice cream cakes.
- **Size Options**: Small, Medium, Large for each product.
- **Flavors**: Vanilla, Strawberry, and Chocolate available for all items.
- **Toppings**: Choose from chocolate, marshmallows, sprinkles, or candies to customize your dessert.
- **Donation Option**: Option to donate an extra dollar with your order.
- **Total Order Calculation**: Displays the total cost of each order and the overall cost.

## Installation 🛠️
No installation is required to run this program. Simply run the Python script, and you can start placing orders.

### Prerequisites
- Python 3.x installed on your machine.
- No external libraries or dependencies required.

## How to Run the Program 🖥️

1. Download the script (e.g., `ordering_system.py`).
2. Open a terminal or command prompt in the directory where the file is located.
3. Run the script using Python:
   ```bash
   python ordering_system.py
   ```

4. The program will prompt you to input the number of orders, followed by user-specific details like name, quantity, product choice, and customizations.
5. After all orders are placed, the program will display the total cost and ask if you’d like to donate $1 to a good cause.
6. It will then display the final cost and a thank-you message.

## How It Works 📝

### Order Process
- **Step 1**: You can order a cake, ice cream, or ice cream cake by choosing the respective option.
- **Step 2**: For each item, you'll be asked to choose:
  - **Size**: Small (`s`), Medium (`m`), Large (`l`).
  - **Flavor**: Vanilla, Strawberry, or Chocolate.
  - **Topping**: Chocolate, Marshmallows, Sprinkles, or Candies.
- **Step 3**: After making your choices, the program calculates the price for your order.
- **Step 4**: You can choose to donate an extra $1 for charity.
- **Step 5**: The program will display the total cost for all orders.

### Sample Order Flow:
1. The user is prompted to select an item: `cake`, `icecream`, or `icecream cake`.
2. The user enters the quantity and customizes the order by selecting the size, flavor, and topping.
3. The program computes the cost of each order and adds it to the total.
4. After all orders, the program asks if the user would like to donate an additional $1 to their order.
5. The program displays the final total and prints a thank-you message.

### Example Run:

```
How many orders do you want to place?
2
Enter your name for Order #1
John
What would you like to order cake, icecream or icecream cake?
cake
How many cakes do you want?
2
What size do you want?(use s,m,l accordingly)
m
What flavor would you like?
chocolate
What topping do you want?
sprinkles
Your per order cost is $ 16
Order completed for John

Enter your name for Order #2
Jane
What would you like to order cake, icecream or icecream cake?
icecream
How many icecreams do you want?
1
What size do you want?
l
What flavor would you like?
vanilla
What topping do you want?
chocolate
Your per order cost is $ 4
Order completed for Jane

Would you like to donate $1?
yes
Your new total is: $ 21
Thanks For Shopping With Us!
```

## Code Breakdown 📊

- **Data Structure**:
  - `cakes`, `icecreams`, `icecreamcake`: Dictionaries storing the cost of each size.
  - `toppings`, `flavors`: Dictionaries for available toppings and flavors.
  - `checkout`: A list to store the names of customers.

- **Functions**:
  - `order(user_name, index)`: Main function that starts the ordering process.
  - `cake(user_name, index)`: Handles cake orders.
  - `icecream(user_name, index)`: Handles ice cream orders.
  - `ice_cream_cake(user_name, index)`: Handles ice cream cake orders.
  - `donate(quantitycost)`: Adds a donation to the total order cost.

## Contributions 🤝

Feel free to fork this project, suggest improvements, or report any bugs. If you have ideas for new features, open an issue or submit a pull request!

## License 📝

This project is open-source and available under the [MIT License](LICENSE).

---

### Next Steps:
- Customize the system further by adding more products, sizes, and features.
- Consider saving orders to a file or database for future reference.
- Add unit tests for better functionality and reliability.

