print("Caesar Cipher")
print("1. Encrypt")
print("2. Decrypt (try all shifts)")
choice = input("Enter 1 or 2: ")

if choice == "1":
    message = input("Enter message: ")
    key = int(input("Enter key (1-25): "))
    result = ""
    for char in message:
        if char.isalpha():
            base = ord('a') if char.islower() else ord('A')
            new_char = chr((ord(char) - base + key) % 26 + base)
            result = result + new_char
        else:
            result = result + char
    print("Encrypted message:", result)

elif choice == "2":
    message = input("Enter encrypted message: ")
    print("Trying all possible shifts:")
    for key in range(1, 26):
        result = ""
        for char in message:
            if char.isalpha():
                base = ord('a') if char.islower() else ord('A')
                new_char = chr((ord(char) - base - key) % 26 + base)
                result = result + new_char
            else:
                result = result + char
        print("Shift", key, ":", result)

else:
    print("Invalid choice")

