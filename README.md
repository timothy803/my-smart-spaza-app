````python
def  hello( ) :
     print (" hello from my file" )
# Umdala  MSME  App - Core  Logic
# Run this with :  python  Umdala.py

import  Json
Impport os
from datetime Import  datetime

DATA_FILE =  "umdala_data.Json"

#Load data or create default
def  load_data():
        if  os.path.exists(DATA_FILE):
        with  open(DATA_FILE, "r") as f:
        return  Json.Load(f)
return {
   "inventory": {
       "bread": {"price":15.0, "qty": 20} ,
       "milk": {"price": 25.0, "qty": 10
       "airtime_10":  {"price": 10.0,  "qty": 50
   },
   "sales_today": 0.0,
   "cash_in_till": 0.0
   "sales_log":  []
}

def save_data(data):
    with open(DATA_FILE, "w") as f
         Json.dump(data, f, indent=2

data = load_data()
inventory = data["inventory"]
sales_today = data["sales_today]
cash_in_till = data["cash_in_till"]
sales_log = data["sales_log]

def show_menu()
    print("\=== UMDALA MSME APP ===")
    print("1. View Inventory")
    print("2. Sell item")
    print("3. Add Stock")
    print("4. Daily Report")
    print("5. Daily report")
    print("6  Exit")
    return  input("choose an option:  ")

def view_inventory()
    print("\n--- current inventory---")
def sell_item( ):
    global  sales_today, cash_in_till

    view_inventory()
    item = input("Enter item name to: ").lower()
    if item not in invetory:
        print("item not found!")
        return

    try:
         qty = int(input("Enter  quantity:
    except  ValueError:
        print(f"Not  enough stock! Only {inventory[item]['qty']} left")
        return

    if inventory[item]["qty"] < qty:
        print(f"Not enough stock! Only  {invetory[item]['qty']} left")

    price = inventory[item]["price"]
    total = price *  qty

    #update data
    invetory[item]["qty]  -= qty
    sales_today  += total
    cash_in_till  + total

    
    
     

