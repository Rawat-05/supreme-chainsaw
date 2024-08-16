# supreme-chainsaw

def caesar_cipher_decoder(text, shift):
    result = ""

    for char in text:
        if char.isalpha():
            ascii_offset = 65 if char.isupper() else 97
            result += chr((ord(char) - ascii_offset - shift) % 26 + ascii_offset)
        else:
            result += char

    return result

text = "Khoor, Zruog!"
shift = 3
print(caesar_cipher_decoder(text, shift))  # Output: "Hello, World!"
