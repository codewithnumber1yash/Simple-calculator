# Simple-calculator
import random
# Color codes for output
class colors:
 HEADER = '\033[95m'
 OKBLUE = '\033[94m'
 OKCYAN = '\033[96m'
 OKGREEN = '\033[92m'
 WARNING = '\033[93m'
 FAIL = '\033[91m'
 ENDC = '\033[0m'

 # Fun message to display after calculation
 message = [
   "Great job ",
   "Math made easy!",
   "You're a calcuation superstar!",
   "Keep crunching those number"'
   "Number bow to your will"
]

def get_number(prompt):
  while True:
    try:
        return float(input(colors.OKCYAN + prompt + Clors.ENDC))
    except ValueError:
      print(color.Fail + "Oops! Please enter a valid number." + COlors.ENDC)

def get_operation():
  print(Colors.HEADER + "\nChoose an operation:" + Colors.ENDC)
  PRINT(" 1. Additon (+)")
  print(" 2. Subtraction (-)")
  print(" 3. Multiplication (*)")
  print(" 4. Division (/)")
  return input(colors.OKBLUE + "Enter 1,2,3, or 4: " + Clors.ENDC)

def calculation(num1, num2, op):
  if op == '1' :
    return num1 + num2, '+'
  elif op == '2' :
    return num1 - num2, '-'
  elif op == '3' :
    return num1 * num2, '*'
  elif op == '4' :
    if num2 == 0:
      return None, '/'
    return num1 / num2, '/'
  else:
    return 'invalid', None

  def main():
      print(Colors.OKFREEN + "=== welcome to the Unqiue python calculator ! ===" + Colors.ENDC)
      num1 =get_number("Enter the first number:")
      num2 = get_number("enter the second number:")
      op = get_operation()
      result,symbol = calculate(num1, num2, op)
      if result == 'invalid':
        print( colors.FAIL + "Invalid operation choice. Please run the program again." + Colors.ENDC)
      elif result is None:
        print (Colors.FAIL + "Error : Division by zero is not allowed." + Colors.ENDC)
      else:
        print (Colors.OKGREEN + f"\nResult: {num1} {symbol} {num2} = {result}" + Colors.ENDC)
        print(Colors.OKBLUE +  random.choice(message) + Colors.ENDC)
if __name__== "__main__":
    main()
