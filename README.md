# CODES_OF_03
import random
import string

def generate_password(length, use_uppercase, use_numbers, use_special_chars):
    characters = string.ascii_lowercase
    if use_uppercase:
        characters += string.ascii_uppercase
    if use_numbers:
        characters += string.digits
    if use_special_chars:
        characters += string.punctuation

    password = ''.join(random.choice(characters) for i in range(length))
    return password

def main():
    print("Random Password Generator")
    length = int(input("Enter the length of the password: "))
    use_uppercase = input("Use uppercase letters? (yes/no): ").lower() == "yes"
    use_numbers = input("Use numbers? (yes/no): ").lower() == "yes"
    use_special_chars = input("Use special characters? (yes/no): ").lower() == "yes"

    password = generate_password(length, use_uppercase, use_numbers, use_special_chars)
    print("Generated Password : ", password)

if __name__ == "__main__":
    main()
