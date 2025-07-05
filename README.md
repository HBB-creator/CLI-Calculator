# CLI-Calculator

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
def mutiply(a, b):
    return a * b
def divide(a, b):
    if b ==0:
        return "Eroor! Division by zero."
    return a / b

print(" standard Python Calculator")
print("Operations: + - * /")

while True:
    try:
        num1 = float(input("Enter first number: "))
        op = input("Choose operation (+, -, *, /): ")
        num2 = float(input("Enter second number: "))

        if op == '+':
            result = add(num1, num2)
        elif op == '-':
            result = subtract(num1, num2)
        elif op == '*':
            result = Multiply(num1, num2)
        elif op == '/':
            result = divide(num1, num2)
        else:
            result = "Invalid operation"

        print(f"Result: {result}")

        again = input("Do you want to calculate again? (y/n): ")
        if again.lower() != 'y':
            break
    except ValueError:
        print("Please enter valid numbers!")
