# hello-world
class goods():
    def __init__(self,number,name,price):
        self.number = number
        self.name = name
        self.price = price

goods_list={}
print("Welcome to this cashier system!")
total = 0
key = input("Please input the number you want to choose:1.add;2.delete;3.calculate;4:quit")
while key!="4":
    if key=="1":
        number = input("Please input the number of goods:")
        name = input("Please input the name of goods:")
        price = input("Please input the price of goods:")
        print("number:"+number+"\tname:"+name.title()+"\tprice:"+price)
        goods_list[number]=goods(name,number,price)
        print(goods_list)
    elif key=="2":
        number = input("Please input the number of goods:")
        name = input("Please input the name of goods:")
        del goods_list[number]
        print(goods_list)
    elif key=="3":
        key2 = "1"
        while key2=="1":
            number = input("Please input the number of goods:")
            quantity = input("Please input the quantity of goods:")
            g_price=int(goods_list[number].price)
            total = total+g_price*int(quantity)
            print(total)
            key2 = input("Please input '1'to continue or input '2' to quit")
    key = input("Please input the number you want to choose:1.add;2.delete;3.calculate;4:quit")
