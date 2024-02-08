import re

def valid(password):
    if not 8<=len(password)<=20:
        return False
    if not re.search("[a-z]",password):
        return False
    if not re.search("[A-Z]",password):
        return False
    if not re.search("[0-9]",password):
        return False
    if not re.search("[!.@#$%^&*()_+]",password):
        return False
    return True
password=input("Enter your password : ")
if valid(password):
    print("Password is valid!")
else:
    print("Password is invalid. Please follow the password requirements.")
    print("""Password must have a :- 
    1. Lower case
    2. Upper case
    3. Number
    4. Symbol""")