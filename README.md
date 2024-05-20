#test code

#random numbergame


import random

def guess_number_game():
    number_to_guess = random.randint(1, 10)
    attempts = 3

    print("数当てゲームへようこそ！1から10までの数を当ててください。")

    while attempts > 0:
        try:
            user_guess = int(input("あなたの予想する数は？: "))
            if user_guess == number_to_guess:
                print("正解です！おめでとうございます！")
                break
            elif user_guess < number_to_guess:
                print("もっと大きい数です。")
            else:
                print("もっと小さい数です。")
            attempts -= 1
            print(f"あと{attempts}回チャンスがあります。")
        except ValueError:
            print("有効な数値を入力してください。")

    if attempts == 0:
        print(f"残念！正解は{number_to_guess}でした。")

guess_number_game()
