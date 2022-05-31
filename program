import random
lista_pytan = []
dziala = 1
while dziala:
    ile_pytan = int(input("ile chcesz miec pytan? (max20) "))
    print(ile_pytan)
    while len(lista_pytan) != ile_pytan:
        los = random.randint(1, 20)
        if not(los in lista_pytan):
            lista_pytan.append(los)
    print(lista_pytan)
    pkt = 0
    pytania = open("pytania.txt", "r").read().split("\n")  #lista pytan
    odpowiedzi = open("odpowiedzi.txt", "r").read().split("\n") #lista odpowiedzi

    for i in range(len(lista_pytan)): # dla każdego z pola, do pierwszego pola wpisujemy pierwsze z danych i tak dalej
        nr_pytania = lista_pytan[i]
        print(f"pytanie nr {lista_pytan[i]}: \n" + pytania[nr_pytania-1]) 
        odpowiedz = input("Twoja dpowiedz: ")
        if odpowiedz == odpowiedzi[nr_pytania-1]:
            pkt +=1
            print(f"Poprawna odpowiedź! Aktualny wynik to {pkt}/{ile_pytan}\n")
        else:
            print(f"Twoja odpowiedz jest bledna! Prawidlowa odpowiedz to:\n{odpowiedzi[nr_pytania-1]}")
            
        if not(int(input("czy chcesz kontynuowac test? 1/0 "))):
            break
    print(f"Zakonczyles test z wynikiem {100*pkt/ile_pytan} %")
    dziala = int(input("chcesz zaczac od nowa? 1/0 "))
print("do zobaczenia byku!")
