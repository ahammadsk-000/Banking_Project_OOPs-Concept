# Banking_Project_OOPs-Concept


# parent class
class User:
    def __init__(self,name,age,gender):
        self.name= name
        self.age = age
        self.gender = gender
    def show_details(self):
        print("Personal details :")

        print("Name     ",self.name)
        print("Age      ",self.age)
        print("Gender    ",self.gender)


# Child class
class Bank(User):
    def __init__(self,name,age,gender):
        super().__init__(name,age,gender)
        self.balance =0
    def deposit(self,amount):
        self.amount= amount
        self.balance += amount
        print("Account balance has been updated  $", self.balance)
    def withdraw(self,w_amount):
        self.w_amount = w_amount
        if w_amount> self.balance:
            print("Insufficient Balance  | Balance available $",self.balance)
        else:
            self.balance -= w_amount
            print("Your withdrew money", w_amount)
            print("your account balance is ", self.balance)
    def view_balance(self):
        self.show_details()
        print("Your account balance is  $",self.balance)



a = Bank("Mahesh",25,"Male")
a.deposit(10000)
a.deposit(20000)
a.withdraw(5000)
a.view_balance()
