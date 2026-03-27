# 🤖 AI'ın Önerdiği Sorular (55 Soru)
> Ders içeriğine dayalı, sınavda çıkabilecek ek sorular. Detaylı teknik açıklamalar içerir.

🏠 [[🏠 Ana Sayfa]] | Hoca soruları → [[Sınav Soruları - Hoca]]

---

## BÖLÜM A — Kod Çıktısı Tahmin Et

---

**S1. Aşağıdaki kodun çıktısı nedir?**
```python
x = 10
x += 5
x *= 2
print(x)
```
**Cevap:** `30`
- `x = 10` → x=10
- `x += 5` → x=15
- `x *= 2` → x=30

---

**S2. Çıktı ne olur?**
```python
print(10 // 3, 10 % 3)
```
**Cevap:** `3 1`
- `10 // 3` = 3 (tam bölüm)
- `10 % 3` = 1 (kalan)

---

**S3. Çıktı ne olur?**
```python
for i in range(2, 10, 3):
    print(i, end=" ")
```
**Cevap:** `2 5 8`
- 2 → 5 → 8 → 11 (11 ≥ 10, dur)

---

**S4. Çıktı ne olur?**
```python
x = 5
y = 10
print(x > 3 and y < 5)
```
**Cevap:** `False`
- `x > 3` → True
- `y < 5` → `10 < 5` → False
- `True and False` → False

---

**S5. Çıktı ne olur?**
```python
def f(x):
    return x * x

print(f(3) + f(4))
```
**Cevap:** `25`
- `f(3)` = 9, `f(4)` = 16 → 9+16 = 25

---

**S6. Çıktı ne olur?**
```python
sayi = 7
if sayi % 2 == 0:
    print("Çift")
else:
    print("Tek")
```
**Cevap:** `Tek`
- `7 % 2` = 1, `1 == 0` → False → else çalışır

---

**S7. Çıktı ne olur?**
```python
toplam = 0
for i in range(1, 6):
    toplam += i
print(toplam)
```
**Cevap:** `15`
- 1+2+3+4+5 = 15

---

**S8. Çıktı ne olur?**
```python
x = 15
if x > 10:
    if x > 20:
        print("Büyük")
    else:
        print("Orta")
else:
    print("Küçük")
```
**Cevap:** `Orta`
- `15 > 10` → True, içeri gir
- `15 > 20` → False → else: "Orta"

---

**S9. Çıktı ne olur?**
```python
i = 0
while i < 3:
    print(i * 2)
    i += 1
```
**Cevap:**
```
0
2
4
```

---

**S10. Çıktı ne olur?**
```python
print(not True or False)
```
**Cevap:** `False`
- `not True` → False
- `False or False` → False

---

## BÖLÜM B — Hata Bulma

---

**S11. Bu kodda hata var mı?**
```python
sayi1 = int(input("1. sayı: "))
sayi2 = int(input("2. sayı: "))
print("Toplam: " + sayi1 + sayi2)
```
**Cevap:** Evet, **tip hatası.** String ile int `+` ile birleştirilemez.
```python
print("Toplam:", sayi1 + sayi2)         # veya
print("Toplam: " + str(sayi1 + sayi2))  # str'e çevir
```

---

**S12. Bu kodda ne yanlış?**
```python
x = 5
if x > 3
    print("Büyük")
```
**Cevap:** `if` satırının sonunda `:` eksik → **SyntaxError**

---

**S13. Bu kod ne hata verir?**
```python
def topla(a, b):
    return a + b

sonuc = topla(3)
```
**Cevap:** `TypeError: topla() missing 1 required positional argument: 'b'`  
Fonksiyon 2 parametre bekliyor, 1 gönderilmiş.

---

**S14. Bu kod neden yanlış çalışır?**
```python
toplam = 0
i = 1
while i <= 5:
    toplam += i
print(toplam)
```
**Cevap:** `i += 1` yok → **sonsuz döngü**. Program hiç bitmez.

---

**S15. Bu kodun sonucu beklenen mi?**
```python
a = "3"
b = "5"
print(a + b)
```
**Cevap:** Hayır. Çıktı `35` (string birleştirme). Sayı toplamak için:
```python
print(int(a) + int(b))   # → 8
```

---

## BÖLÜM C — Program Yazma

---

**S16. Kullanıcıdan 3 sayı alıp en büyüğünü bulan program yazın (for olmadan).**

**Cevap:**
```python
a = float(input("1. sayı: "))
b = float(input("2. sayı: "))
c = float(input("3. sayı: "))

en_buyuk = a
if b > en_buyuk:
    en_buyuk = b
if c > en_buyuk:
    en_buyuk = c

print("En büyük:", en_buyuk)
```

---

**S17. 1'den 100'e kadar çift sayıların toplamını bulun.**

**Cevap:**
```python
toplam = 0
for i in range(2, 101, 2):
    toplam += i
print("Çift sayılar toplamı:", toplam)   # 2550
```

---

**S18. Klavyeden sayı alarak, 0 girilince duran ve toplamı yazan program yazın.**

**Cevap:**
```python
toplam = 0
sayi = int(input("Sayı (0=dur): "))
while sayi != 0:
    toplam += sayi
    sayi = int(input("Sayı (0=dur): "))
print("Toplam:", toplam)
```

---

**S19. Bir sayının asal olup olmadığını kontrol eden program yazın.**

**Cevap:**
```python
sayi = int(input("Sayı: "))
asal = True
if sayi < 2:
    asal = False
else:
    for i in range(2, sayi):
        if sayi % i == 0:
            asal = False

if asal:
    print(f"{sayi} asal sayıdır")
else:
    print(f"{sayi} asal değildir")
```

---

**S20. Kullanıcıdan iki sayı alıp GCD (EBOB) bulan program yazın.**

**Cevap:**
```python
a = int(input("a: "))
b = int(input("b: "))
while b != 0:
    a, b = b, a % b
print("EBOB:", a)
```
> 💡 Bu Öklid algoritmasıdır — for döngüsü yerine while kullanımına güzel örnektir.

---

## BÖLÜM D — Kavramsal Sorular

---

**S21. `int(3.9)` ile `round(3.9)` arasındaki fark nedir?**

**Cevap:**
- `int(3.9)` → `3` (kesir kısmını **atar**, yuvarlamaz)
- `round(3.9)` → `4` (en yakın tam sayıya **yuvarlar**)

---

**S22. Python'da `True` ve `False` sayısal değerleri nedir?**

**Cevap:**
- `True` = 1
- `False` = 0

```python
print(True + True)    # 2
print(True * 5)       # 5
print(False + 10)     # 10
```

---

**S23. `not` operatörü ne yapar? Örnek verin.**

**Cevap:** Boolean değerin tersini alır.
```python
not True    # False
not False   # True
not (5 > 3) # not True → False
not (5 > 9) # not False → True
```

---

**S24. Bir fonksiyon `return` kullanmazsa ne döner?**

**Cevap:** `None` döner.
```python
def f():
    x = 5

sonuc = f()
print(sonuc)    # None
```

---

**S25. `range(5)` ile `range(0, 5)` aynı mı?**

**Cevap:** Evet, tamamen aynı çıktıyı üretir: `0, 1, 2, 3, 4`

---

**S26. `for` döngüsünde `range` yerine başka şey kullanılabilir mi?**

**Cevap:** Evet, string ve liste üzerinde de dönülebilir.
```python
for harf in "Python":
    print(harf)
# P y t h o n
```

---

**S27. Fonksiyon içinde tanımlanan değişkene dışarıdan erişilebilir mi?**

**Cevap:** Hayır. Fonksiyon içindeki değişkenler **yerel (local)** kapsama sahiptir.
```python
def f():
    x = 10

f()
print(x)   # NameError! x burada tanımsız
```

---

**S28. `round(2.5)` sonucu nedir? Neden?**

**Cevap:** Python 3'te `2` (banker's rounding / yuvarlak sayıya en yakın çift). Bu bazen sürpriz olabilir. `round(3.5)` → `4`.

---

**S29. `print()` ile `return` arasındaki fark nedir?**

**Cevap:**
- `print()` → Değeri **ekrana yazdırır**, fonksiyondan dışarıya vermez
- `return` → Değeri **çağırana gönderir**, ekrana yazmaz

```python
def kare_print(n):
    print(n * n)       # ekrana yazar ama kaybolur

def kare_return(n):
    return n * n       # değer kullanılabilir kalır

x = kare_return(5)    # x = 25
y = kare_print(5)     # y = None (return yok)
```

---

**S30. `//` ve `/` arasındaki fark nedir?**

**Cevap:**
- `/` → Her zaman **float** döner
- `//` → **Tam sayı** sonuç döner (kesir atılır)

```python
7 / 2     # 3.5  (float)
7 // 2    # 3    (int, kesir atıldı)
```

---

## BÖLÜM E — İleri Sorular

---

**S31. İki değişkenin değerini üçüncü değişken kullanmadan nasıl değiştirirsiniz?**

**Cevap:** Python'da tuple unpacking ile:
```python
a, b = 3, 7
a, b = b, a
print(a, b)   # 7 3
```

---

**S32. `while True:` ne demektir? Sonsuz döngü müdür?**

**Cevap:** Evet, koşul her zaman True olduğu için sonsuz döngüdür. Ancak içinde `break` ile çıkılabilir.
```python
while True:
    giris = input("Devam (E/H)? ")
    if giris == "H":
        break   # döngüden çık
```

---

**S33. Faktöriyel hesaplayan fonksiyon yazın.**

**Cevap:**
```python
def faktoriyel(n):
    sonuc = 1
    for i in range(1, n + 1):
        sonuc *= i
    return sonuc

print(faktoriyel(5))   # 120
```

---

**S34. String veri tipi üzerinde hangi işlemler yapılabilir?**

**Cevap:**
```python
s = "Merhaba"
len(s)          # 7 (uzunluk)
s.upper()       # "MERHABA"
s.lower()       # "merhaba"
s[0]            # "M" (ilk karakter)
s + " Dünya"    # "Merhaba Dünya" (birleştirme)
```

---

**S35. `f-string` nedir? Nasıl kullanılır?**

**Cevap:** Formatlı string oluşturma yöntemi. Değişkenleri `{}` içine yazarak metin içinde kullanılır.
```python
ad = "Ali"
yas = 20
print(f"Merhaba {ad}, yaşın {yas}")
print(f"5 kare = {5**2}")
print(f"Pi = {3.14159:.2f}")   # 2 ondalık basamak
```

---

**S36. Aşağıdaki kodda kaç kez döner?**
```python
i = 10
while i > 0:
    i -= 3
    print(i)
```
**Cevap:** 4 kez. i = 7, 4, 1, -2 (son adımda -2 ≤ 0, döngü biter)

---

**S37. `def` anahtar kelimesi ne anlama gelir?**

**Cevap:** "Define" (tanımla) anlamında. Python'a "bir fonksiyon tanımlıyorum" sinyali verir.

---

**S38. Birden fazla değer döndüren fonksiyon mümkün müdür?**

**Cevap:** Evet, tuple ile döndürülür.
```python
def min_max(a, b, c):
    return min(a,b,c), max(a,b,c)

kucuk, buyuk = min_max(3, 1, 7)
print(kucuk, buyuk)   # 1 7
```

---

**S39. `%` operatörü ile bir sayının çift olup olmadığı nasıl kontrol edilir?**

**Cevap:**
```python
sayi = int(input("Sayı: "))
if sayi % 2 == 0:
    print("Çift")
else:
    print("Tek")
```
Mantık: Çift sayılar 2'ye tam bölünür → kalan 0.

---

**S40. `for` döngüsünde değişken adı önemli midir?**

**Cevap:** Herhangi bir geçerli isim kullanılabilir. Geleneksel olarak `i`, `j`, `k` tercih edilir. Kullanılmayacaksa `_` yazılır.
```python
for _ in range(3):
    print("Merhaba")   # 3 kez yazdır, sayaç kullanılmıyor
```

---

**S41. `import math` neden kullanılır?**

**Cevap:** Python'un `math` modülü matematiksel fonksiyonlar içerir. `sqrt`, `pi`, `ceil`, `floor` gibi. Bunları kullanmak için önce import edilmeli.
```python
import math
print(math.sqrt(144))   # 12.0
print(math.ceil(3.2))   # 4
print(math.floor(3.9))  # 3
```

---

**S42. Sıcaklık dönüşümü: Kullanıcıdan Celsius alıp Fahrenheit'a çeviren program yazın.**

**Cevap:**
```python
c = float(input("Celsius: "))
f = (c * 9/5) + 32
print(f"{c}°C = {f}°F")
```

---

**S43. Aşağıdaki `if-elif-else` zincirini okuyun ve girdi 85 için çıktıyı söyleyin.**
```python
puan = 85
if puan >= 90:
    print("AA")
elif puan >= 80:
    print("BA")
elif puan >= 70:
    print("BB")
else:
    print("Düşük")
```
**Cevap:** `BA`
- `85 >= 90` → False
- `85 >= 80` → True → "BA" yazdır, diğerleri kontrol edilmez

---

**S44. Aynı fonksiyon farklı tipte parametreler alabilir mi?**

**Cevap:** Python dinamik tipli olduğu için evet, ancak fonksiyon içindeki işlemler tipe bağlı hata verebilir.
```python
def iki_kat(x):
    return x * 2

print(iki_kat(5))       # 10   (int)
print(iki_kat("Ali"))   # AliAli (str tekrar!)
```

---

**S45. 1'den N'e kadar sayıların karesini yazdıran fonksiyon yazın.**

**Cevap:**
```python
def kareler(n):
    for i in range(1, n + 1):
        print(f"{i}^2 = {i**2}")

kareler(5)
# 1^2 = 1
# 2^2 = 4
# 3^2 = 9
# 4^2 = 16
# 5^2 = 25
```

---

## BÖLÜM F — 🪤 Tuzaklı Sorular (Dikkat!)

> Bu sorular sınavda sizi yanıltmak için tasarlanmış tarzda. Hoca bu tarz örnekleri seviyor.

---

**S46. Çıktı ne olur?**
```python
x = "5"
y = 3
print(x * y)
```
**Cevap:** `555`
- ⚠️ TUZAK: `x` string! `"5" * 3` → string'i 3 kez tekrarlar.
- `5 * 3 = 15` DEĞİL! Tip dönüşümü yapılmadı.

---

**S47. Bu kod hata verir mi?**
```python
x = 10
if x > 5:
    print("Büyük")
    print("devam")
print("bitti")
```
**Cevap:** Hata vermez. Çıktı:
```
Büyük
devam
bitti
```
- ⚠️ TUZAK: `print("bitti")` if'in **dışında** — girintisi yok. Her durumda çalışır.

---

**S48. Çıktı ne olur?**
```python
for i in range(5):
    pass
print(i)
```
**Cevap:** `4`
- ⚠️ TUZAK: `pass` hiçbir şey yapmaz ama `i` değişkeni hâlâ son değerini tutar.
- `range(5)` → son değer 4.

---

**S49. Çıktı ne olur?**
```python
print(10 / 5)
```
**Cevap:** `2.0` (**2 değil!**)
- ⚠️ TUZAK: `/` operatörü **her zaman float** döner. `2` değil `2.0`.
- `int` sonuç istiyorsan `//` kullan: `10 // 5` → `2`

---

**S50. Bu iki kod aynı sonucu verir mi?**
```python
# Kod 1
x = 5
if x > 3:
    print("A")
if x > 1:
    print("B")

# Kod 2
x = 5
if x > 3:
    print("A")
elif x > 1:
    print("B")
```
**Cevap:** Hayır!
- **Kod 1:** İki ayrı `if` → ikisi de kontrol edilir → `A` ve `B` yazdırır
- **Kod 2:** `elif` kullanılmış → ilk doğru olan çalışır → sadece `A` yazdırır
- ⚠️ TUZAK: `if-if` ile `if-elif` farklı çalışır!

---

**S51. Bu kodda mantık hatası var mı?**
```python
toplam = 0
for i in range(1, 11):
    toplam += 1
print("1-10 toplamı:", toplam)
```
**Cevap:** Evet! Çıktı `10` verir, `55` değil.
- ⚠️ TUZAK: `toplam += 1` yazılmış, `toplam += i` olmalıydı!
- Bu bir **mantık hatası** — program çalışır ama yanlış sonuç verir. Yorumlayıcı fark etmez.

---

**S52. Çıktı ne olur?**
```python
def topla(a, b):
    c = a + b

sonuc = topla(3, 5)
print(sonuc)
```
**Cevap:** `None`
- ⚠️ TUZAK: `return` yok! Fonksiyon hesaplıyor ama sonucu **döndürmüyor**.
- `c = a + b` yerel kalır, dışarıya çıkmaz.

---

**S53. `range(1, 1)` kaç kez döner?**

**Cevap:** **0 kez** (hiç dönmez)
- ⚠️ TUZAK: Başlangıç = bitiş olunca döngü hiç çalışmaz.
- Benzer: `range(5, 3)` → hiç çalışmaz (artım pozitif ama bitiş < başlangıç)

---

## BÖLÜM G — Eksik Konular (Düşük olasılıklı ama hocanın bahsettiği)

---

**S54. `format()` metodu nedir? Örnek verin.**

**Cevap:** Metin içine değişken yerleştirmek için kullanılır:
```python
print("{} {} yaşında".format("Ali", 20))
# → Ali 20 yaşında

# Sıra numarası ile
print("{1} ve {0}".format("A", "B"))
# → B ve A
```
> 💡 Sınavda çıkma olasılığı düşük — f-string daha yaygın. Ama hoca Hafta 7'de anlattı.

---

**S55. `0.1 + 0.2 == 0.3` sonucu nedir? Neden?**

**Cevap:** `False`!
```python
print(0.1 + 0.2)        # 0.30000000000000004
print(0.1 + 0.2 == 0.3) # False
```
- Bilgisayar ikilik (binary) sistemde çalışır, bazı ondalıklı sayılar tam temsil edilemez.
- Çözüm: `round(0.1 + 0.2, 1) == 0.3` → `True`
> 💡 Sınavda çıkma olasılığı düşük ama hoca Hafta 6'da bu konudan bahsetti.

