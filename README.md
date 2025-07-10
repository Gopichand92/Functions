# Functions
def add(a,b):
    return a+b
student1=int(input("Enter the money:"))
student2=int(input("Enter the money:"))
total=add(student1,student2)
print("total amount:",total)
OUTPUT:
      Enter the money:3000
      Enter the money:4000
      total amount: 7000
---------------------------------------------------------------
  ef value():
    return 3.14159
result=value()
print("value in the function is",result)
 OUTPUT:   value in the function is 3.14159
 ------------------------------------------------------------
 def get_name():
    name=input("Enter your name:")
    return name
username=get_name()
print("WElCOME",username)
OUTPUT:
Enter your name: Y.S.JAGANMOHAN REDDY
WElCOME Y.S.JAGANMOHAN REDDY
-----------------------------------------------------------------
def info(name='unknown',age=0):
    print("Name:",name)
    print("Age:",age)
info("Gopi",21)
info("Chandu")
info(age=21)
info()
OUTPUT:
Name: Gopi
Age: 21
Name: Chandu
Age: 0
Name: unknown
Age: 21
Name: unknown
Age: 0
--------------------------------------------------------------------
def cal(a,b):
    return a+b,a-b,a*b,a/b
a=int(input("Enter a:"))
b=int(input("Enter b:"))
sum,diff,pro,div=cal(a,b)
print("Sum",sum)
print("Subtract",diff)
print("Product",pro)
print("Divide",div)
OUTPUT:
Enter a: 44
Enter b: 2
Sum 46
Subtract 42
Product 88
Divide 22.0
--------------------------------------------------------------------------
  
