# Restaurant Menu 

Basically you seen many hotel menu and menu cards and it's also hotel menu it menu take a order then ask you want to next order so please enter a second order then it program sum orders to cost then it show your total bill and it is a simple program but help full 

__Here are same statement of this program__
 +  while loop
 +  If statement 
 +  string
 +  dictionary
 +  lower 
 +  strip




```python
hotel_menu = {
    "pasta": 200,
    "burger": 100,
    "pizza": 300,
    "chicken wings": 150,
    "mango juice": 100,
}

print("Welcome To Our Restaurant!")
print("""
Restaurant Menu
----------------
pasta: Rs. 200
burger: Rs. 100
pizza: Rs. 300
chicken wings: Rs. 150
mango juice: Rs. 100
""")

total_cost = 0

while True:
    item_1 = input("Hello dear, may I help you? What would you like to order? ").lower().strip() #Strip to remove leading/trailing spaces
    if item_1 in hotel_menu:
        print(f"Your item '{item_1}' has been added in your order.") # Corrected item_2 to item_1
        total_cost += hotel_menu[item_1]
    else:
        print(f"Sorry, we don't have '{item_1}' on the menu. Please choose from the menu.")

    more_order = input("Do you want to order more? (Yes/No): ").strip().lower()
    if more_order == "no":
        print("Thank you very much for buying!")
        print(f"Your total cost is Rs. {total_cost}")
        break
    elif more_order == "yes":
        item_2 = input("Enter a more order?").lower().strip() #Strip to remove leading/trailing spaces
        print(f"Your item '{item_2}' has been added to your order.")
        
        # Check if item_2 is in menu before accessing its price
        if item_2 in hotel_menu:
            total_cost += hotel_menu[item_2]
        else:
            print(f"Sorry, we don't have '{item_2}' on the menu. Please choose from the menu.")
        
        print("Thank you very much for buying!")
        print(f"Your total cost is Rs. {total_cost}")        

        break
```