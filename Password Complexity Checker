import re

def check_length(password):
    return len(password) >= 8

def check_lowercase(password):
    return any(char.islower() for char in password)

def check_uppercase(password):
    return any(char.isupper() for char in password)

def check_digit(password):
    return any(char.isdigit() for char in password)

def check_special_char(password):
    special_chars = re.compile('[@_!#$%^&*()<>?/\|}{~:]')
    return special_chars.search(password) is not None

def assess_password_strength(password):
    strength = 0
    
    if check_length(password):
        strength += 1
    else:
        print("Password should be at least 8 characters long.")

    if check_lowercase(password) and check_uppercase(password):
        strength += 1
    else:
        print("Password should contain both uppercase and lowercase letters.")

    if check_digit(password):
        strength += 1
    else:
        print("Password should contain at least one digit.")

    if check_special_char(password):
        strength += 1
    else:
        print("Password should contain at least one special character.")

    if strength == 4:
        print("Password is strong.")
    elif strength >= 2:
        print("Password is moderate.")
    else:
        print("Password is weak.")

def main():
    password = input("Enter your password: ")
    assess_password_strength(password)

if __name__ == "__main__":
    main()
