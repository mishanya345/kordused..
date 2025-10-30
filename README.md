import random

# 1️ Majade kuvamine
def print_houses(n):
    house = [
        "  ~~~~~  ",
        " /_____\\ ",
        " | []  | ",
        "  -----  "
    ]
    
    for i in range(len(house)):
        line = ""
        for j in range(n):
            line += house[i]
            if j < n - 1:
                line += " "
        print(line)

# 2️ Klasside keskmised hinded
def average_grades():
    klass1_hinded = [4, 3, 5, 4, 3, 5, 4, 2, 4, 5]
    klass2_hinded = [3, 4, 4, 5, 3, 4, 5, 4, 3, 4]
    
    sum1 = 0
    sum2 = 0
    
    for hinne in klass1_hinded:
        sum1 += hinne
    
    for hinne in klass2_hinded:
        sum2 += hinne
    
    keskmine1 = sum1 / len(klass1_hinded)
    keskmine2 = sum2 / len(klass2_hinded)
    
    print(f"Klassi 1 keskmine hinne: {keskmine1:.2f}")
    print(f"Klassi 2 keskmine hinne: {keskmine2:.2f}")

# 3️ Minimaalne ja maksimaalne hinne
def min_max_hinded():
    hinded = [4.5, 3.2, 5.0, 4.1, 3.8, 4.9, 2.5, 4.7, 3.9, 5.0]
    
    min_hinne = hinded[0]
    max_hinne = hinded[0]
    
    for hinne in hinded:
        if hinne < min_hinne:
            min_hinne = hinne
        if hinne > max_hinne:
            max_hinne = hinne
    
    print(f"Minimaalne hinne: {min_hinne}")
    print(f"Maksimaalne hinne: {max_hinne}")

# 4️ Rahvastikutihedus
def rahvastikutihedus():
    vallad = []
    
    for i in range(12):
        elanikud = random.randint(2, 50)
        pindala = random.randint(100, 500)
        vallad.append((elanikud, pindala))
    
    kogu_elanikud = 0
    kogu_pindala = 0
    
    for elanikud, pindala in vallad:
        kogu_elanikud += elanikud
        kogu_pindala += pindala
    
    keskmine_tihedus = (kogu_elanikud * 1000) / kogu_pindala
    
    print(f"Kokku: {kogu_elanikud}t elanikku, {kogu_pindala} km²")
    print(f"Keskmine rahvastikutihedus: {keskmine_tihedus:.2f} elanikku/km²")

# 5️ Funktsiooni tabel
def funktsiooni_tabel():
    x_min = 1
    x_max = 3
    samm = 0.5
    
    print("x\t| y")
    print("--------")
    
    x = x_min
    while x <= x_max + 0.0001:
        y = -0.5 * x + x
        print(f"{x}\t| {y:.2f}")
        x += samm

# Käivitamine
print("1. Majade kuvamine:")
print_houses(3)

print("\n2. Klasside keskmised hinded:")
average_grades()

print("\n3. Min ja max hinded:")
min_max_hinded()

print("\n4. Rahvastikutihedus:")
rahvastikutihedus()

print("\n5. Funktsiooni tabel:")
funktsiooni_tabel()
