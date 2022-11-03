import random
my_list = [23, 30, 45, 90, 71, 73, 92, 55, 13, -55, 2, -79,
           94, -83, 40, -9, 82, 41, -81, -84, -100, -84, 2, 56, -93, 83,
           69, 31, -95, 71, 36, 75, -100, 98, -48, -98, 41, -61, 86, 28,
           -16, 94, 88, -100, 55, -66, 88, -72, 94, 11, 66, -63, -81, 58,
           -23, -78, 86, -100, 57, -86, -37, -31, 70, -51, 60, -41, 30, 6,
           -5, 36, 92, -73, 40, -93, -74, 21, -15, 39, 60, 95, 81, -71, 3, 35,
           -9, -9, 75, 40, -81, 20, -39, -34, -29, 99, 46, 95, -80, -81, -44, -91]


# 8.

def nieparzyste(a):
    suma = 0
    for x in a:
        if x % 2 != 0:
            suma += x
    return(suma)


# 9.

def dzielenia5i7(a):
    suma = 0
    for x in a:
        if x % 5 == 0 and x % 7 == 0:
            suma += x
    return(suma)


# 10.


def pytanie(a):
    liczby = 0
    pyt = input("Podaj liczbę : ")
    pyt = int(pyt)
    for x in a:
        if x == pyt:
            liczby += 1
    return(liczby)


# 11.


def maxmin(a):
    lmax = []
    lmin = []
    ma = max(a)
    mi = min(a)
    for x in range(len(a)):
        if a[x] == ma:
            lmax.append(x)
        if a[x] == mi:
            lmin.append(x)
    return(lmax, lmin)


# 12.


def customlista():
    dlugosc = int(input("Podaj długośc listy : "))
    zakres1 = int(input("Podaj zakres listy od : "))
    zakres2 = int(input("Podaj zakres listy do : "))
    clista = []
    for x in range(dlugosc):
        clista.append(random.randint(zakres1, zakres2))
    return(clista)


# ______WYWOŁANIA______
print("zadanie 8")
print(nieparzyste(my_list))
print("zadanie 9")
print(dzielenia5i7(my_list))
print("zadanie 10")
print(pytanie(my_list))
print("zadanie 11")
print(maxmin(my_list))
print("zadanie 12")
print(customlista())
