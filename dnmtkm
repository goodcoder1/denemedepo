import random

def main():
    while True:
        print("Taş, Kağıt, Makas oyununa hoş geldiniz!")
        print("1. Taş")
        print("2. Kağıt")
        print("3. Makas")
        print("4. Oyundan Çık")

        user_choice = input("Lütfen seçiminizi yapın (1-4): ")

        if user_choice == '4':
            print("Oyundan çıkılıyor...")
            break
        elif user_choice not in ['1', '2', '3']:
            print("Geçersiz seçim! Lütfen 1, 2, 3 veya 4 seçeneklerinden birini seçin.")
            continue

        user_choice = int(user_choice)
        computer_choice = random.randint(1, 3)

        print("Sizin seçiminiz:", get_choice_name(user_choice))
        print("Bilgisayarın seçimi:", get_choice_name(computer_choice))

        winner = determine_winner(user_choice, computer_choice)
        if winner == 0:
            print("Berabere!")
        elif winner == 1:
            print("Tebrikler! Kazandınız.")
        else:
            print("Maalesef, bilgisayar kazandı.")

def get_choice_name(choice):
    if choice == 1:
        return "Taş"
    elif choice == 2:
        return "Kağıt"
    else:
        return "Makas"

def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return 0  # Berabere
    elif (user_choice == 1 and computer_choice == 3) or \
         (user_choice == 2 and computer_choice == 1) or \
         (user_choice == 3 and computer_choice == 2):
        return 1  # Kullanıcı kazandı
    else:
        return 2  # Bilgisayar kazandı

if __name__ == "__main__":
    main()
