# Пример кода на Python: Генератор случайных паролей

import random
import string

def generate_password(length=12):
    """Генерирует случайный пароль заданной длины"""
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

if __name__ == "__main__":
    password_length = int(input("Введите длину пароля (по умолчанию 12): "))
    if password_length <= 0:
        print("Длина пароля должна быть больше 0. Используется длина по умолчанию (12).")
        password_length = 12

    generated_password = generate_password(password_length)
    print("Сгенерированный пароль:", generated_password)
