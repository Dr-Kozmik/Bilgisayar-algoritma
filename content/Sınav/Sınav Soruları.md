# 🎯 Sınav Soruları — Index

🏠 [[🏠 Ana Sayfa]] | Hızlı bakış → [[Cheat Sheet]]

---

## Temel Sorular

**S1. 3 hata türü nedir? Farkları nedir?**
→ [[Konular/Hata Türleri]]

**S2. `=` ile `==` arasındaki fark nedir?**
- `=` → Atama (`x = 5`)
- `==` → Karşılaştırma (`x == 5` → True/False)

**S3. `int()`, `float()`, `str()` ne zaman kullanılır?**
```python
sayi = int(input("Sayı: "))     # input string döner, dönüştür
x = float(input("Ondalık: "))  # virgüllü sayı için
print("Sonuç: " + str(42))     # sayıyı metinle birleştir
```

**S4. `//` ve `%` ne yapar? Örnek verin.**
```python
17 // 5   # = 3   (kaç tam 5 var?)
17 % 5    # = 2   (kalan ne?)
```

**S5. Değişken isimlendirme kuralları nelerdir?**
→ [[Konular/Değişkenler ve Veri Tipleri]]

---

## Orta Seviye Sorular

**S6. `and`, `or`, `not` doğruluk tablolarını yazın.**
→ [[Konular/Koşul Yapıları (if-elif-else)]]

**S7. `range(1, 10, 2)` hangi değerleri üretir?**
```
1, 3, 5, 7, 9
```

**S8. for ile while farkı nedir?**
→ [[Konular/Döngüler (for-while)]]

**S9. Aşağıdaki kodun çıktısı nedir?**
```python
x = 7
if x > 5 and x < 10:
    print("Aralıkta")
else:
    print("Dışarıda")
```
**Cevap:** `Aralıkta` (7 > 5 ✅ ve 7 < 10 ✅, ikisi de True → and → True)

**S10. `del x` ne yapar?**
```python
x = 10
del x
print(x)   # NameError!
```

---

## İleri Seviye Sorular

**S11. Aşağıdaki programın çıktısı nedir?**
```python
def kare(n):
    return n * n

for i in range(1, 4):
    print(kare(i))
```
**Cevap:** `1` sonra `4` sonra `9`

**S12. Sonsuz döngü neden oluşur? Nasıl önlenir?**
```python
# Hatalı (sonsuz döngü!)
i = 0
while i < 5:
    print(i)
    # i += 1 UNUTULMUŞ!

# Doğru
i = 0
while i < 5:
    print(i)
    i += 1
```

**S13. Fahrenheit → Celsius dönüşüm programı yazın.**
```python
f = float(input("Fahrenheit: "))
c = (f - 32) * 5/9
print(f"Celsius: {c:.2f}")
```

**S14. Kullanıcıdan 5 sayı alıp toplamını bulan program yazın.**
```python
toplam = 0
for i in range(5):
    sayi = float(input(f"{i+1}. sayıyı giriniz: "))
    toplam += sayi
print("Toplam:", toplam)
```

**S15. Sayının tek mi çift mi olduğunu bulun.**
```python
sayi = int(input("Sayı: "))
if sayi % 2 == 0:
    print("Çift")
else:
    print("Tek")
```
