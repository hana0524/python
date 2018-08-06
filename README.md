#python
print("Hello World")

print("kobukuro")

# !/usr/bin/env python
# -*- coding:utf-8 -*-

import random

dic = {"a":"ぐー","b":"チョキ","c":"パー"}

print("ジャンケン...")
print("a=グー b=チョキ c=パー  aかbかcを入力")
user = input('>>>  ')
user = user.lower()

try:
    user_choice = dic[user]

    choice_list = ["a","b","c"]
    pc = dic[random.choice(choice_list)]

    draw = 'DRAW'
    win = 'win'
    lose = 'lose'

    if user_choice == pc:
        judge = draw
    else:
        if user_choice == "グー":
            if pc == "チョキ":
                judge = win
            else:
                judge = lose
        elif user_choice == "チョキ":
            if pc == "パー":
                judge = win
            else:
                judge = lose
        else:
            if pc == "グー":
                judge = win
            else:
                judge = lose


    print("あなたが選んだのは%s"% user_choice)
    print("コンピューターが選んだのは%s"% pc)
    print("結果は%s"% judge)
except:
    print("何か入力して下さい")

