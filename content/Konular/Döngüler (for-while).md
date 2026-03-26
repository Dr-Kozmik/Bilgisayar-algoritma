# Döngüler (for - while)

🏠 [[🏠 Ana Sayfa]] | Kaynak: [[Haftalar/Hafta 7]] · [[Haftalar/Hafta 9]]

---

## for Döngüsü

```python
for i in range(başlangıç, bitiş, artım):
    # kod
```

### range() Örnekleri (Sınavda Çıkar!)
```python
range(5)          # 0 1 2 3 4
range(1, 6)       # 1 2 3 4 5       (6 dahil değil!)
range(1, 11, 2)   # 1 3 5 7 9       (ikişer atla)
range(10, 0, -1)  # 10 9 8 ... 1    (azalan)
```

### Kod Örnekleri
```python
# 1'den 10'a kadar topla
toplam = 0
for i in range(1, 11):
    toplam += i
print("Toplam:", toplam)   # 55

# Çift sayıları listele
for i in range(2, 21, 2):
    print(i, end=" ")      # 2 4 6 8 10 12 14 16 18 20
```

---

## while Döngüsü

```python
while koşul:
    # kod
    # sayacı güncelle!
```

> ⚠️ Sayacı unutursanız **sonsuz döngü!**

### Kod Örnekleri
```python
# 1'den 5'e kadar say
i = 1
while i <= 5:
    print(i)
    i += 1      # UNUTMA!

# Kullanıcı 0 girene kadar topla
toplam = 0
sayi = int(input("Sayı (0 = dur): "))
while sayi != 0:
    toplam += sayi
    sayi = int(input("Sayı (0 = dur): "))
print("Toplam:", toplam)
```

---

## for vs while

| | `for` | `while` |
|--|-------|---------|
| **Ne zaman?** | Kaç kez döneceğini biliyorsan | Koşula bağlıysa |
| **Sayaç** | Otomatik | Elle artır |
| **range()** | Gerekli | Gerekli değil |
| **Sonsuz döngü riski** | Yok | Var (sayacı unutursan) |

---

## İç İçe Döngü (Nested Loop)

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(i, "x", j, "=", i*j)
```
> 💡 AI Notu: İç içe döngü çarpım tablosu, matris işlemleri için kullanılır.
