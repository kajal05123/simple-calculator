# simple-calculator
#python
import math
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    return x / y
def atan2(x,y):
    return atan(y/x)
def hypot(x,y):
    return sqrt(x*x + y*y)
def gcd(x,y):
    return gcd(y,x%y)
print("Select operation.")
print("1.Add")
print("2.Subtract")
print("3.Multiply")
print("4.Divide")
print("5.atan(y/x)")
print("6.hypot(x,y)")
print("7.gcd(y,x%y)")
while True:
    
    choice = input("Enter choice(1/2/3/4/5/6/7): ")
    if choice in ('1', '2', '3', '4','5','6','7'):
        num1 = int(input("Enter first number: "))
        num2 = int(input("Enter second number: "))

        if choice == '1':
            print(num1, "+", num2, "=", add(num1, num2))

        elif choice == '2':
            print(num1, "-", num2, "=", subtract(num1, num2))

        elif choice == '3':
            print(num1, "*", num2, "=", multiply(num1, num2))

        elif choice == '4':
            print(num1, "/", num2, "=", divide(num1, num2))
        elif choice == '5':
            print("math.atan2(",num1,",",num2,"): ", math.atan2(num1,num2))
        elif choice == '6':
            print("math.hypot(",num1,",",num2,"): ", math.hypot(num1,num2))
        elif choice == '7':
            print("math.gcd(",num1,",",num2,"): ", math.gcd(num1,num2))
        
        next_calculation = input("Let's do next calculation? (yes/no): ")
        if next_calculation == "no":
          break
    
    else:
        print("Invalid Input")
