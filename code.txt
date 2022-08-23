#calculator 
def add(n1, n2):
  return n1 + n2

def subtract(n1, n2):
  return n1 - n2

def multiply(n1, n2):
  return n1 * n2

def divide(n1, n2):
  return n1 / n2

operations = {
  "+": add,
  "-": subtract,
  "*": multiply,
  "/": divide
}

num1 = int(input("Enter first number -> "))
num2 = int(input("Enter second number -> "))

for symbol in operations:
  print(symbol)

operation_symbol = input("Pick an operation from the line above: ")
calculation_function = operations[operation_symbol]
first_answer = calculation_function(num1, num2)

print(f"{num1} {operation_symbol} {num2} = {first_answer}")

operation_symbol = input("pick another operation: ")
num3 = int(input("What's the next number?: "))
calculation_function = operations[operation_symbol]
next_answer = calculation_function(first_answer, num3)

print(f"{first_answer} {operation_symbol} {num3} = {next_answer}")