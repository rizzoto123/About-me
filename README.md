# About-me
import os

logpass="logpass.txt"

def user():
    users={}
    if os.path.exists(logpass):
        with open("logpass.txt","r", encoding="utf-8") as myfile:
            for line in myfile:
                login,password = line.strip().split(":")
                users[login]=password
    return users

def save_user(login,password):
    with open("logpass.txt","a", encoding="utf-8") as myfile:
        myfile.write(f"{login}:{password}\n")
aaa=user()
print(aaa)

while True:
    qqq=(input("1-Зарегистрироваться\n2-Войти:"))
    if qqq=="1":
        login = input("Логин:")
        password = input("Пароль:")
        print("Вы зарегистрировались")
        save_user(login,password)
        break
    if qqq=="2":
        login = input("Логин:")
        password = input("Пароль:")
    if login not in aaa and password not in aaa:
        print("Повторите позже")
        break
    else:
        print("Вы вошли")
        break

while True:
    ppp=(input("1-Обо мне\n2-Моя цель\n3-Выход:"))
    if ppp=="1":
        print("Меня зовут Олжас.\n Мне 15 лет.\n Я занимаюсь прогрммированием уже более 2 месяцев.\n О Cap-edu я узнал благодаря их конференции в апреле.\n Мой ментор Абильмансур тичер.\n В свободное время я люблю играть в компьютерные игры.\n")
    if ppp=="2":
        print("Моя цель-стать программистом.\nНа данный момент я остановился на проектной работе 2")
    if ppp=="3":
        break
