# Caesar-
def caesar_cipher(text, shift, direction='encrypt'):
    result = ""
    
    if direction == 'decrypt':
        shift = -shift

  
    for i in range(len(text)):
        char = text[i]
    
        if char.isupper():
            result += chr((ord(char) + shift - 65) % 26 + 65)
   elif char.islower():
            result += chr((ord(char) + shift - 97) % 26+ 97) 
   else:
            result += char
    return result
message = "Hello, World!"
shift = 3

encrypted_message = caesar_cipher(message, shift)
print(f"Encrypted: {encrypted_message}")

decrypted_message = caesar_cipher(encrypted_message, shift, 'decrypt')
print(f"Decrypted: {decrypted_message}")
