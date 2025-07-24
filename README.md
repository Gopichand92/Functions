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
  def value():
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
 def eo(numbers):
    e=0
    o=0
    for n in numbers:
        if n %2==0:
            e+=1
        else:
            o+=1
    return e,o
num=input("Enter number of space seperated:")
num_list=list(map(int,num.split()))
e,o=eo(num_list)
print("Even Count:",e)
print("Odd Count:",o)
OUTPUT:
Enter number of space seperated: 8 66 90 888 45 2 167 46 
Even Count: 6
Odd Count: 2
----------------------------------------------------------------------------
def outer():
    print("This is a outer function.......")
    def inner():
        print("this is an inner function........")
    inner()
outer()   
OUTPUT:
This is a outer function.......
this is an inner function........
-----------------------------------------------------------------------------------
def cal(a,b):
    def add():
        return a+b
    def sub():
        return a-b
    def mul():
        return a*b
    print("Addition",add())
    print("Subtract",sub())
    print("product",mul())
a=int(input("Enter a number:"))
b=int(input("Enter a number:"))
cal(a,b)
OUTPUT:
Enter a number: 5
Enter a number: 5
Addition 10
Subtract 0
product 25
-------------------------------------------------------------------------------------------
def mul_by(n):
    def inner(x):
        return x*n
    return inner
times_2= mul_by(2)
times_3= mul_by(3)
print(times_2(5))
print(times_3(10))
 OUTPUT:
 10
30
-----------------------------------------------------------------------------------------
def greet(text):
    def inner(name):
        return f"{text},{name}!!!!!!"
    return inner 
hi=greet('Hello')
print(hi('Yaar'))
OUTPUT:
Hello,Yaar!!!!!!
-------------------------------------------------------------------------------------
fact=1
def factorial(n):
    global fact
    fact=1
    for i in range(1,n+1):
        fact*=i
    return fact
num=int(input("Enter a number:"))
if num<0:
    print("cannot derive for -ve number")
else:
    factorial (num)
    print(f"factorial of {num} is",fact )
OUTPUT:
Enter a number: 6
factorial of 6 is 720
------------------------------------------------------------------------------------
def info(**kwargs):
    for key,value in kwargs.items():
        print(f"{key}:{value}")
info(name='gopi',age=21,cgpa=7.20)
OUTPUT:
name:gopi
age:21
cgpa:7.2
------------------------------------------------------------------------------

def factorial(n):
    if n==0 or n==1:
        return 1
    return n*factorial(n-1)
num=int(input("Enter the value:"))
value = factorial(num)
print(value)
OUTPUT:
Enter the value: 4
24
------------------------------------------------------------------------------------
def sum(n):
    if n==0:
        return 0
    return n+sum(n-1)
num=int(input("enter the number"))
print(f"sum of first {num} numbers is {sum(num)}")
OUTPUT:
enter the number 2
sum of first2 numbers is 3
------------------------------------------------------------------------------------
def retext(c):
    if len(c)==0:
        return c
    return retext(c[1:])+c[0]
text=input("Enter a word:")
print(f"Reverse the word {text} is {retext(text)}")
OUTPUT:
Enter a word: utnihc o/w unam
Reverse the word utnihc o/w unam is manu w/o chintu
--------------------------------------------------------------------------------------
def sumnum(*args):
    print(args[4])
    return sum(args)
print(sumnum(1,2,3,4,5,6,7,8,9,10))
OUTPUT:
5
55
------------------------------------------------------------------------------------
#fibonacci 0 1 1 2 3 5 8 13 21 34 55
def fib(n):
    if n<=1:
        return n
    else:
        return fib(n-1)+fib(n-2)
num=int(input("enter term:"))
for i in range(num):
    print(fib(i),end=' ')
OUTPUT:
enter term: 10
0 1 1 2 3 5 8 13 21 34
------------------------------------------------------------------------------------------
def dsum(n):
    if n==0:
        return 0
    return n%10 + temp(n//10)
def temp(n):
    return dsum(n)
num=int(input("enter a 4 digit number:"))
print("sum of digits:",dsum(num))
OUTPUT:
enter a 4 digit number: 1245
sum of digits: 12
--------------------------------------------------------------------------------------------
def one(n):
    if n==0:
        return True
    else:
        return two(n-1)
def two(n):
    if n==0:
        return False
    else:
        return one(n-1)
num=int(input("enter a number:"))
if one(num):
    print(num,"is even")
else:
    print(num,"is odd")
OUTPUT:
enter a number: 68
68 is even
---------------------------------------------------------------------------------------------
def A(n):
    if n<=0:
        return
    print("Gopi",n)
    B(n-1)
def B(n):
    if n<=0:
        return
    print("Parikela",n)
    A(n-1)
num=int(input("Enter a number:"))
A(num)
OUTPUT:
Enter a number: 11
Gopi 11
Parikela 10
Gopi 9
Parikela 8
Gopi 7
Parikela 6
Gopi 5
Parikela 4
Gopi 3
Parikela 2
Gopi 1
-------------------------------------------------------------------------------------------------
def fib(n):
    if n<=1:
        return n
    return fib(n-1)+fib(n-2)
terms=int(input("Enter number of terms to print:"))
print(("fibonacci series....."))
for i in range(terms):
    print(fib(i),end=' ')
OUTPUT:
Enter number of terms to print: 6
fibonacci series.....
0 1 1 2 3 5 
-------------------------------------------------------------------------------------------------
''' permutations of char in tree recursion '''

def permute(s, bucket=''):
    if not s:
        print(bucket)
        return
    for i in range(len(s)):
        ns=s[:i]+s[i+1:]
        permute(ns,bucket+s[i])
        
text=input("Enter a name/word: ")
print("possibilities of combinations.....")
permute(text)
OUTPUT:
Enter a name/word:  abc
possibilities of combinations.....
abc
acb
bac
bca
cab
cba
--------------------------------------------------------------------------------------------------
 
