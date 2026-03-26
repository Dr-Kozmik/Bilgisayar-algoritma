# ⚡ Cheat Sheet — Hızlı Referans

🏠 [[🏠 Ana Sayfa]] | Sınav soruları → [[Sınav Soruları]]

---

```python
# ── VERİ TİPLERİ ──────────────────────────────────────
x = 5          # int
x = 3.14       # float
x = "Ali"      # str
x = True       # bool

type(x)        # tipi öğren
int("5")       # → 5
float("3.7")   # → 3.7
str(100)       # → "100"

# ── GİRİŞ / ÇIKIŞ ─────────────────────────────────────
ad = input("Ad: ")                     # str gelir!
sayi = int(input("Sayı: "))            # int için
ondalik = float(input("Ondalık: "))   # float için

print("Merhaba", ad)
print(f"Sayı: {sayi}")
print("A", "B", sep="-")    # A-B
print("X", end=" ")         # alt satıra geçmez

# ── DEĞİŞKEN ──────────────────────────────────────────
del x          # bellekten sil
a = b = 0     # çoklu atama
x, y = 1, 2  # tuple atama

# ── ARİTMETİK OPERATÖRLER ─────────────────────────────
# +  -  *  /  //  %  **
5 // 2    # 2  (tam bölme)
5 % 2     # 1  (kalan)
2 ** 3    # 8  (üs)

# Öncelik: () > ** > * / // % > + -

# Kısaltmalı: += -= *= /= //= %=

# ── KARŞILAŞTIRMA ─────────────────────────────────────
# == != > < >= <=   →  True / False
# = atama,  == karşılaştırma!

# ── MANTIK OPERATÖRLERI ───────────────────────────────
# and → ikisi True ise True
# or  → biri True ise True
# not → tersini al

# ── KOŞULLAR ──────────────────────────────────────────
if x > 0:
    print("Pozitif")
elif x == 0:
    print("Sıfır")
else:
    print("Negatif")

# ── for DÖNGÜSÜ ───────────────────────────────────────
for i in range(1, 11):      # 1..10
    print(i)

for i in range(0, 20, 2):   # 0,2,4,...,18
    print(i)

# ── while DÖNGÜSÜ ─────────────────────────────────────
i = 1
while i <= 10:
    print(i)
    i += 1    # UNUTMA!

# ── FONKSİYON ─────────────────────────────────────────
def topla(a, b):
    return a + b

sonuc = topla(3, 5)   # 8

# ── HAZIR FONKSİYONLAR ────────────────────────────────
abs(-5)          # 5
round(3.7)       # 4
max(3, 7, 2)     # 7
min(3, 7, 2)     # 2
pow(2, 3)        # 8

import math
math.sqrt(25)    # 5.0

# ── YORUMLAR ──────────────────────────────────────────
# Bu satır çalışmaz
x = 5  # satır sonu yorumu
```

---

## Hata Türleri (Ezbere!)

| | Söz Dizimi | Çalışma Zamanı | Mantık |
|-|---|----|---|
| Program çalışır mı? | ❌ | Başlar, durur | ✅ (yanlış) |
| Yorumlayıcı bulur mu? | ✅ | ✅ | ❌ |

## range() (Ezbere!)
```
range(n)        → 0 ... n-1
range(a, b)     → a ... b-1     (b dahil değil!)
range(a, b, k)  → a, a+k, a+2k... (b'ye kadar)
```
