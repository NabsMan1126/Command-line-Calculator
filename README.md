# Command-line-Calculator
A simple Python CLI calculator for basic arithmetic operations.
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error: Cannot divide by zero"
    return a / b


def main():
    print("Simple Command-Line Calculator")
    print("Operations: +, -, *, /")

    while True:
        try:
            num1 = float(input("Enter first number: "))
            operator = input("Enter operator: ")
            num2 = float(input("Enter second number: "))

            if operator == "+":
                print("Result:", add(num1, num2))
            elif operator == "-":
                print("Result:", subtract(num1, num2))
            elif operator == "*":
                print("Result:", multiply(num1, num2))
            elif operator == "/":
                print("Result:", divide(num1, num2))
            else:
                print("Invalid operator")

        except ValueError:
            print("Invalid input. Please enter numbers only.")

        again = input("Do another calculation? (y/n): ").lower()
        if again != "y":
            break


if __name__ == "__main__":
    main()
