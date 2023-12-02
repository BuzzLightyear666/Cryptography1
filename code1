# Функція шифрування
def xor_encrypt(input_text, key_tuple, shift):
    encrypted_text = [] 

    for i in range(len(input_text)):                                 # Використовуеться для кожного введеного символу 
        key_byte = key_tuple[i % len(key_tuple)]                     # Визначається байт ключа для поточного символу
        encrypted_byte = (ord(input_text[i]) + shift) ^ key_byte     # Шифрування символа 
        encrypted_text.append(encrypted_byte)                        # Додавання зашифрованих байтів у список

    encrypted_text_str = ''.join(chr(byte) for byte in encrypted_text)  # Перетворення списку зашифрованих байтів в строку

    return encrypted_text_str

# Функція розшифрування
def xor_decrypt(encrypted_text, key_tuple, shift):
    decrypted_text = []

    for i in range(len(encrypted_text)):                            # Використовуеться для кожного введеного символу
        key_byte = key_tuple[i % len(key_tuple)]                    # Визначається байт ключа для поточного символу
        decrypted_byte = chr((ord(encrypted_text[i]) ^ key_byte) - shift)    # Розшифрування символа 
        decrypted_text.append(decrypted_byte)                       # Розшифрований символ додається до списку

    decrypted_text_str = ''.join(decrypted_text)                    # Перетворення списку розшифрованих байтів в строку

    return decrypted_text_str

# Функція виконання
def main(): 
    while True:                                        
        input_text = input("Введіть вхідний текст: ")                 # Ввод тексту
        key_tuple = (52, 3, 0)                                        # Ввод кортежу байтів, що використовуються як ключ для операції XOR, за варіантом №1
        shift = int(input("Введіть сдвиг строки: "))                  # Ввод сдвигу

        encrypted_text = xor_encrypt(input_text, key_tuple, shift)     # Виконується та виводиться шифрування символів
        print("Зашифрований текст:", encrypted_text) 

        decrypted_text = xor_decrypt(encrypted_text, key_tuple, shift)    # Виконується та виводиться розшифрування символів
        print("Розшифрований текст:", decrypted_text) 

if __name__ == "__main__":                                                # Конструкція, яка дозволяє виконувати скрипт тільки при запуску файлу безпосередньо, а не при імпорті в інший скрипт.
    main()
