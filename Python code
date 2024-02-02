# Function to convert decimal to binary
def decimal_to_binary(decimal):
    decimal = int(decimal)
    binary = ""
    if decimal == 0:
        return "0"
    while decimal != 0:
        binary = str(decimal % 2) + binary
        decimal //= 2

    return binary

# Function to convert decimal to octal
def decimal_to_octal(decimal):
    octal_digits = "01234567"
    octal = ""
    decimal = int(decimal)
    while decimal  != 0:
        remainder = decimal % 8
        octal = octal_digits[remainder] + octal
        decimal //= 8

    return octal

# Function to convert decimal to hexadecimal
def decimal_to_hexadecimal(decimal):
    decimal = int(decimal)

    hex_digits = "0123456789ABCDEF"
    hexadecimal = ""
    while decimal > 0:
        remainder = decimal % 16
        hexadecimal = hex_digits[remainder] + hexadecimal
        decimal //= 16

    return hexadecimal

# Function to convert binary to decimal
def binary_to_decimal(binary):
    binary=int(binary)
    decimal = 0
    power = 0
    while binary != 0:
        decimal += (binary % 10) * (2 ** power)
        binary //= 10
        power += 1

    return decimal

# Function to convert octal to decimal
def octal_to_decimal(octal):
    octal=str(octal)
    decimal = 0
    power = 0
    for digit in octal[::-1]:
        decimal += int(digit) * (8 ** power)
        power += 1

    return decimal

# Function to convert hexadecimal to decimal
def hexadecimal_to_decimal(hexadecimal):
    hex_digits = "0123456789ABCDEF"
    hexadecimal = hexadecimal.upper()
    decimal = 0
    power = 0
    for digit in reversed(hexadecimal):
        if digit in hex_digits:
            decimal += hex_digits.index(digit) * (16 ** power)
            power += 1
        else:
            print(f"Invalid hex digit: {digit}")
            return None

    return decimal

"""
The following four functions are responsible for checking if the user input is 
is valid with the chosen base.
"""

def is_binary(s):
    for char in s:
        if char not in ['0', '1']:
            return False
        
    return True

def is_octal(s):
    valid_octal_digits = set('01234567')
    for char in s:
        if char not in valid_octal_digits:
            return False
        
    return True

def is_hexadecimal(s):
    valid_hex_digits = "0123456789ABCDEF"
    for char in s:
        if char.upper() not in valid_hex_digits:
            return False
        
    return True

def is_decimal(s):
    
    return s.isdigit()

"""The following three functions are responsible for showing the user the menu
they are currently on.
"""
def display_menu_1():
    print("\n** Numbering System Converter **")
    print("A) Insert a new number")
    print("B) Exit program\n")

def display_menu_2():
    print("\n** Please select the base you want to convert a number from **")
    print("A) Decimal")
    print("B) Binary")
    print("C) Octal")
    print("D) Hexadecimal")

def display_menu_3():
    print("\n** Please select the base you want to convert a number to **")
    print("A) Decimal")
    print("B) Binary")
    print("C) Octal")
    print("D) Hexadecimal")
    
# Main function to drive the program
def main():
    while True:
        display_menu_1()
        choice_1 = input("Enter your choice(A/B): ").upper()

        if choice_1 == 'A':
            display_menu_2()
            choice_2 = input("\nEnter your choice(A/B/C/D): ").upper()
            
            if choice_2 == 'A':
                while True:
                    number = input("\nEnter a VALID decimal number : ")
                    
                    if is_decimal(number):
                        break
                    else:
                        print("The input is not a decimal number. Please try again.")
                        
            elif choice_2 == 'B':
                while True:
                    number = input("\nEnter a VALID binary number : ")
                    
                    if is_binary(number):
                        break
                    else:
                        print("The input is not a binary number : ")
                        
            elif choice_2 == 'C':
                while True:
                    number = input("\nEnter an VALID octal number : ")
                    
                    if is_octal(number):
                        break
                    else:
                        print("The input is not an octal number. Please try again.")
                        
            elif choice_2 == 'D':
                while True:
                    number = input("\nEnter a VALID hexadecimal number : ")
                    
                    if is_hexadecimal(number):
                        break
                    else:
                        print("The input is not a hexadecimal number. Please try again.")
                
            if choice_2 in ['A', 'B', 'C', 'D']:
                display_menu_3()
                choice_3 = input("\nEnter your choice(A/B/C/D): ").upper()

                if choice_3 in ['A', 'B', 'C', 'D']:
                    if choice_2 == 'A':

                        if choice_3 == 'B':
                            base_from = decimal_to_binary(number)

                        elif choice_3 == 'C':
                            base_from = decimal_to_octal(number)
                            
                        elif choice_3 == 'A':
                            base_from = number    

                        elif choice_3 == 'D':
                            base_from = decimal_to_hexadecimal(number)

                    elif choice_2 == 'B':

                        if choice_3 == 'A':
                            base_from = binary_to_decimal(number)
                           
                        elif choice_3 == 'B':
                            base_from = number    

                        elif choice_3 == 'C':
                            base_from = decimal_to_octal(binary_to_decimal(number))

                        elif choice_3 == 'D':
                            base_from = decimal_to_hexadecimal(binary_to_decimal(number))

                    elif choice_2 == 'C':

                        if choice_3 == 'A':
                            base_from = octal_to_decimal(number)

                        elif choice_3 == 'B':
                            base_from = decimal_to_binary(octal_to_decimal(number))
                            
                        elif choice_3 == 'C':
                            base_from = number    

                        elif choice_3 == 'D':
                            base_from = decimal_to_hexadecimal(octal_to_decimal(number))

                    elif choice_2 == 'D':

                        if choice_3 == 'A':
                            base_from = hexadecimal_to_decimal(number)

                        elif choice_3 == 'B':
                            base_from = decimal_to_binary(hexadecimal_to_decimal(number))

                        elif choice_3 == 'C':
                            base_from = decimal_to_octal(hexadecimal_to_decimal(number))
                            
                        elif choice_3 == 'D':
                            base_from = number    

                    print(f"\nResult: {base_from}")
                    
                else:
                    print("Please select a valid choice.")
                    
            else:
                print("Please select a valid choice.")
                
        elif choice_1 == 'B':
            print("Exiting program.")
            break #used to exit the main program
        else:
            print("Please select a valid choice.")
    
            
# Run the main function
main()
