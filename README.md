# Python-ass-1
def calculate(num1, num2, operation):
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        if num2 == 0:
            return "Error: Division by zero is undefined."
        else:
            return num1 / num2
    else:
        return "Invalid operation."

def main():
    print("Welcome to the simple calculator!")
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (+, -, *, /): ")
        result = calculate(num1, num2, operation)
        if isinstance(result, str):
            print(result)
        else:
            print(f"{num1} {operation} {num2} = {result}")
    except ValueError:
        print("Error: Please enter valid numbers.")

if __name__ == "__main__":
    main()

