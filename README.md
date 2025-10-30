# 1. Majad
n = 3
maja = ["   ~~~~~   ","  /_____\\  ","  | []  |  ","   -----   "]
for rida in maja:
    print((rida + " ") * n)

# 2. Keskmised hinded
klass1 = [4, 3, 5, 4, 3]
klass2 = [5, 4, 3, 5, 4]
print("Klass 1:", sum(klass1)/len(klass1))
print("Klass 2:", sum(klass2)/len(klass2))

# 3. Min ja max
hinded = [4.5, 3.2, 5.0, 4.1, 3.8]
min_h = hinded[0]
max_h = hinded[0]
for h in hinded:
    if h < min_h: min_h = h
    if h > max_h: max_h = h
print("Min:", min_h, "Max:", max_h)

# 4. Rahvastikutihedus
elanikud = [15, 8, 22, 5, 30, 12, 18, 7, 25, 10, 20, 14]
pindala = [120, 80, 150, 60, 200, 100, 130, 70, 180, 90, 160, 110]
kogu_inimesed = sum(elanikud) * 1000
kogu_pindala = sum(pindala)
tihedus = kogu_inimesed / kogu_pindala
print("Tihedus:", round(tihedus, 2))

# 5. Funktsioon
x_min, x_max, samm = 1, 3, 0.5
x = x_min
while x <= x_max:
    y = -0.5*x + x
    print(f"x={x} y={y}")
    x += samm 
