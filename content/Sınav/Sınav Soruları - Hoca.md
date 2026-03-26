# 🔴 Hocanın Sorabilecekleri (55 Soru)
> Transkriptlerde hocanın **"sınavda çıkabilir"**, **"bunu bilin"**, **"mutlaka sorarım"** dediği konulardan.

🏠 [[🏠 Ana Sayfa]] | AI soruları → [[Sınav Soruları - AI]]

---

## BÖLÜM 1 — Temel Kavramlar

---

**S1. Algoritma nedir? Özellikleri neler olmalıdır?**

**Cevap:** Bir problemi çözmek için belirlenmiş adım adım süreçtir.
- **Kesinlik:** Her adım net, belirsizlik yok
- **Sonluluk:** Sonunda mutlaka biter
- **Etkinlik:** Adımlar uygulanabilir

*Hoca örneği:* Binada kazı → demir → beton sırası. Sıra değişirse mantık hatası oluşur.

---

**S2. Derleyici (Compiler) ile Yorumlayıcı (Interpreter) arasındaki fark nedir? Python hangi kategoridedir?**

**Cevap:**
- **Derleyici:** Tüm kodu önce makine diline çevirir, sonra çalıştırır (C, C++)
- **Yorumlayıcı:** Satır satır okur, çevirir ve hemen çalıştırır (**Python**)

Python bir **yorumlayıcı** dilidir. Hatalar çalışma sırasında satır satır bulunur.

---

**S3. Python'daki 3 hata türünü yazın ve aralarındaki farkı açıklayın.**

**Cevap:**

| | Söz Dizimi | Çalışma Zamanı | Mantık |
|-|---|----|---|
| Ne zaman? | Çalışmadan önce | Çalışırken | Her zaman |
| Yorumlayıcı bulur mu? | ✅ Evet | ✅ Evet | ❌ Hayır |
| Program çalışır mı? | ❌ | Başlar, durur | ✅ (ama yanlış) |

**Söz Dizimi:** `print("Merhaba"` → parantez kapanmamış  
**Çalışma Zamanı:** `5 / 0` → ZeroDivisionError  
**Mantık:** Formülü ters yazmak → program çalışır ama cevap yanlış

*Hoca vurgusu:* "Mantık hatalarını yorumlayıcı bulamaz, en zor hata türü budur."

---

**S4. Söz dizimi hatasına 3 örnek verin.**

**Cevap:**
```python
print("Merhaba"      # Parantez kapanmamış
if x > 5             # İki nokta (:) eksik
x = = 5              # Yanlış operatör yazımı
```

---

**S5. Çalışma zamanı hatasına 2 örnek verin.**

**Cevap:**
```python
sayi = int("abc")    # ValueError — metin sayıya çevrilemiyor
print(tanimsiz)      # NameError — değişken tanımlanmamış
```

---

**S6. Mantık hatasını söz dizimi hatasından nasıl ayırt edersiniz?**

**Cevap:** Söz dizimi hatası programı **çalıştırmaz**, hata mesajı verir. Mantık hatası programı **çalıştırır** ama yanlış sonuç üretir. Yorumlayıcı mantık hatasını hiç fark etmez.

---

## BÖLÜM 2 — Veri Tipleri ve Değişkenler

---

**S7. Python'daki temel veri tiplerini yazın ve örnek verin.**

**Cevap:**
```python
x = 5        # int   — tam sayı
x = 3.14     # float — ondalıklı
x = "Ali"    # str   — metin
x = True     # bool  — doğru/yanlış
```

---

**S8. `type()` fonksiyonu ne işe yarar?**

**Cevap:** Bir değişkenin veya değerin veri tipini öğrenmek için kullanılır.
```python
x = 42
print(type(x))      # <class 'int'>
print(type("Ali"))  # <class 'str'>
print(type(3.14))   # <class 'float'>
```

---

**S9. `int()`, `float()`, `str()` fonksiyonları ne zaman kullanılır?**

**Cevap:** Tip dönüşümleri (Type Casting) için kullanılır.
```python
int("42")       # "42" → 42   (metni tamsayıya çevir)
float("3.14")   # "3.14" → 3.14
str(100)        # 100 → "100" (sayıyı metne çevir)
int(3.9)        # 3.9 → 3   (kesir atılır, YUVARLANMAZ!)
```

---

**S10. `input()` fonksiyonu hangi veri tipini döndürür? Bu neden önemlidir?**

**Cevap:** `input()` her zaman **str (metin)** döndürür. Sayısal işlem yapılacaksa mutlaka dönüştürülmeli:
```python
# Yanlış:
sayi = input("Sayı: ")
sonuc = sayi + 10      # HATA! str + int yapılamaz

# Doğru:
sayi = int(input("Sayı: "))
sonuc = sayi + 10      # Çalışır
```

---

**S11. Değişken isimlendirme kuralları nelerdir?**

**Cevap:**
- ✅ Harf veya `_` ile başlamalı
- ✅ Harf, rakam ve `_` içerebilir
- ❌ Rakamla başlayamaz: `1sayi`
- ❌ Boşluk içeremez: `benim sayi`
- ❌ Özel karakter yok: `#x`, `@ad`
- ❌ Python anahtar kelimeleri kullanılamaz: `if`, `for`, `while`, `def`
- 🔤 Büyük/küçük harf farklıdır: `Ad ≠ ad`

---

**S12. Aşağıdaki değişken isimlerinden geçerli olanları işaretleyin:**
`1sayi` / `_toplam` / `benim ad` / `elif` / `ogrenci_no` / `#puan`

**Cevap:**
- `1sayi` ❌ (rakamla başlıyor)
- `_toplam` ✅
- `benim ad` ❌ (boşluk var)
- `elif` ❌ (anahtar kelime)
- `ogrenci_no` ✅
- `#puan` ❌ (özel karakter)

---

**S13. `del` komutu ne yapar?**

**Cevap:** Değişkeni bellekten tamamen siler. Silindikten sonra kullanılmaya çalışılırsa `NameError` hatası verir.
```python
x = 10
del x
print(x)    # NameError: name 'x' is not defined
```

---

**S14. `round()` fonksiyonu nasıl kullanılır?**

**Cevap:**
```python
round(3.7)        # 4    (en yakın tam sayıya)
round(3.14159, 2) # 3.14 (2 ondalık basamağa)
round(3.14159, 3) # 3.142
```

---

**S15. Çoklu atama nasıl yapılır?**

**Cevap:**
```python
# Hepsine aynı değeri ata
a = b = c = 0

# Farklı değerleri sırayla ata
x, y, z = 1, 2, 3
print(x, y, z)   # 1 2 3
```

---

## BÖLÜM 3 — Operatörler

---

**S16. `=` ile `==` arasındaki fark nedir?**

**Cevap:**
- `=` → **Atama** operatörü. Sağdaki değeri soldaki değişkene atar.
- `==` → **Karşılaştırma** operatörü. Eşit mi diye sorar, True/False döner.

```python
x = 5        # x'e 5 ata
x == 5       # x, 5'e eşit mi? → True
x == 10      # x, 10'a eşit mi? → False
```

---

**S17. `//` operatörü ne yapar? `%` ne yapar? Örnekle açıklayın.**

**Cevap:**
- `//` → **Tam bölme:** Bölümün tam sayı kısmını verir
- `%` → **Modulo:** Bölme işleminin kalanını verir

```python
17 // 5    # 3  (17'de kaç tam 5 var?)
17 % 5     # 2  (17'yi 5'e böldüğünde kalan)

# Gerçek kullanım: Saniyeyi saate çevir
saniye = 7261
saat   = saniye // 3600    # 2
kalan  = saniye % 3600     # 61 (kalan saniye)
dakika = kalan // 60       # 1
```

---

**S18. Operatör öncelik sırası nedir?**

**Cevap (yüksekten düşüğe):**
1. `()` — Parantez
2. `**` — Üs alma
3. `*`, `/`, `//`, `%` — Çarpma/Bölme
4. `+`, `-` — Toplama/Çıkarma

```python
2 + 3 * 4       # 14  (önce çarpma)
(2 + 3) * 4     # 20  (önce parantez)
2 ** 3 + 1      # 9   (önce üs: 8+1)
```

---

**S19. Kısaltmalı atama operatörlerini yazın.**

**Cevap:**
```python
x = 10
x += 5    # x = x + 5 → 15
x -= 3    # x = x - 3 → 12
x *= 2    # x = x * 2 → 24
x /= 4    # x = x / 4 → 6.0
x //= 2   # x = x // 2 → 3
x %= 2    # x = x % 2 → 1
```

---

**S20. `x += 1` ile `x = x + 1` arasında fark var mıdır?**

**Cevap:** Hayır, ikisi de aynı işlemi yapar. `x += 1` kısa yazımıdır.

---

## BÖLÜM 4 — print() ve input()

---

**S21. `print()` fonksiyonunun `sep` parametresi ne işe yarar?**

**Cevap:** Birden fazla değer yazdırırken aralarına ne konulacağını belirtir. Varsayılan boşluktur.
```python
print("A", "B", "C")          # A B C
print("A", "B", "C", sep="-") # A-B-C
print("A", "B", sep="")       # ABC (boşluksuz)
```

---

**S22. `print()` fonksiyonunun `end` parametresi ne işe yarar?**

**Cevap:** Yazdırma bittikten sonra ne yapılacağını belirtir. Varsayılan `\n` (alt satır).
```python
print("Merhaba", end=" ")
print("Dünya")
# → Merhaba Dünya  (aynı satırda)
```

---

**S23. `#` işareti Python'da ne anlama gelir?**

**Cevap:** Yorum satırı başlatır. O satır program tarafından çalıştırılmaz.
```python
# Bu satır çalışmaz
x = 5  # bu da çalışmaz (satır sonu)
```

---

## BÖLÜM 5 — Koşul Yapıları

---

**S24. `if-else` yapısının sözdizimini yazın.**

**Cevap:**
```python
if koşul:           # iki nokta zorunlu!
    komut1          # 4 boşluk girinti
    komut2
else:
    komut3
```

---

**S25. Girintileme (indentation) neden önemlidir?**

**Cevap:** Python'da küme parantezi `{}` yoktur. Hangi kodun hangi bloğa ait olduğu **girinti** ile belirlenir. Hatalı girinti → `IndentationError`.
```python
if x > 0:
    print("Pozitif")  # if bloğuna ait
print("Her zaman")    # if bloğuna değil
```

---

**S26. `elif` ne zaman kullanılır?**

**Cevap:** Birden fazla koşul kontrol edilecekse. `else if`'in kısaltmasıdır.
```python
puan = 75
if puan >= 90:
    print("AA")
elif puan >= 80:
    print("BA")
elif puan >= 70:
    print("BB")
else:
    print("Düşük")
# → BB
```

---

**S27. Boolean nedir? True ve False değerleri ne anlama gelir?**

**Cevap:** `bool` veri tipidir. `True` (doğru = 1) ve `False` (yanlış = 0) olmak üzere iki değer alır. Koşul ifadelerinin sonucu Boolean üretir.
```python
5 > 3     # True
5 == 10   # False
```

---

**S28. `and`, `or`, `not` operatörlerini doğruluk tablosuyla açıklayın.**

**Cevap:**

| E1 | E2 | E1 and E2 | E1 or E2 | not E1 |
|:--:|:--:|:---------:|:--------:|:------:|
| T | T | **T** | **T** | F |
| T | F | **F** | **T** | F |
| F | T | **F** | **T** | T |
| F | F | **F** | **F** | T |

- `and`: İkisi de True olmalı
- `or`: En az biri True olmalı
- `not`: Tersini alır

---

**S29. `pass` ifadesi ne işe yarar?**

**Cevap:** "Hiçbir şey yapma, devam et" anlamına gelir. Boş bir blok bırakılamayacağı için yer tutucu olarak kullanılır.
```python
if x > 0:
    pass        # şimdilik boş
else:
    print("Negatif")
```

---

**S30. Aşağıdaki kodun çıktısı nedir?**
```python
x = 7
if x > 5 and x < 10:
    print("Aralıkta")
else:
    print("Dışarıda")
```
**Cevap:** `Aralıkta`
- `x > 5` → `7 > 5` → True
- `x < 10` → `7 < 10` → True
- `True and True` → True → if bloğu çalışır

---

**S31. Aşağıdaki kodun çıktısı nedir?**
```python
x, y = 10, 20
if x != 10 and y == 20:
    print("A")
else:
    print("B")
```
**Cevap:** `B`
- `x != 10` → `10 != 10` → False
- `False and ...` → kısa devre → False
- else bloğu çalışır → `B`

---

**S32. Sıfıra bölme hatası nasıl önlenir?**

**Cevap:** Bölme yapmadan önce bölenin sıfır olup olmadığı kontrol edilir:
```python
bolen = int(input("Bölen: "))
if bolen != 0:
    sonuc = 10 / bolen
    print("Sonuç:", sonuc)
else:
    print("Sıfıra bölme yapılamaz!")
```

---

## BÖLÜM 6 — for Döngüsü

---

**S33. `for` döngüsünün sözdizimini yazın.**

**Cevap:**
```python
for değişken in range(başlangıç, bitiş, artım):
    # kod bloğu
```

---

**S34. `range(1, 11)` hangi değerleri üretir?**

**Cevap:** `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`
Bitiş değeri (11) **dahil değildir**.

---

**S35. `range(2, 20, 3)` hangi değerleri üretir?**

**Cevap:** `2, 5, 8, 11, 14, 17` — 20'den büyük olmayan son değer 17.

---

**S36. `range()` ile azalan sırada döngü nasıl yapılır?**

**Cevap:** Artım değeri negatif verilir.
```python
for i in range(10, 0, -1):
    print(i, end=" ")
# → 10 9 8 7 6 5 4 3 2 1
```

---

**S37. `print()`'te `end` parametresi for döngüsüyle nasıl kullanılır?**

**Cevap:**
```python
for i in range(1, 6):
    print(i, end=" ")
# → 1 2 3 4 5  (tüm sayılar aynı satırda)
```

---

**S38. 1'den 10'a kadar olan sayıların toplamını for ile hesaplayın.**

**Cevap:**
```python
toplam = 0
for i in range(1, 11):
    toplam += i
print("Toplam:", toplam)   # 55
```

---

**S39. `range(n)` tek parametre verilince nasıl çalışır?**

**Cevap:** 0'dan başlar, n-1'e kadar gider.
```python
range(5)   # 0, 1, 2, 3, 4
```

---

**S40. Kullanıcıdan alınan N sayısı kadar döngü nasıl kurulur?**

**Cevap:**
```python
n = int(input("Kaç tekrar: "))
for i in range(n):
    print(f"{i+1}. tekrar")
```

---

## BÖLÜM 7 — while Döngüsü

---

**S41. `while` döngüsünün sözdizimini yazın.**

**Cevap:**
```python
while koşul:
    komutlar
    # sayacı güncelle!
```

---

**S42. while döngüsünde sonsuz döngü neden oluşur?**

**Cevap:** Koşul hiç False olmaz — genellikle sayac artırılmayı unutulduğunda.
```python
i = 0
while i < 5:
    print(i)
    # i += 1 unutulmuş → sonsuz döngü!
```

---

**S43. `for` ile `while` döngüsü arasındaki temel fark nedir?**

**Cevap:**
- `for`: Kaç kez döneceği **önceden belli** (range ile)
- `while`: Koşul sağlandığı **sürece** döner, sayı önceden bilinmeyebilir

---

**S44. 1'den 5'e kadar `while` ile yazdırın.**

**Cevap:**
```python
i = 1
while i <= 5:
    print(i)
    i += 1    # zorunlu!
```

---

**S45. Kullanıcı "E" girene kadar tekrar eden program yazın.**

**Cevap:**
```python
giris = ""
sayac = 0
while giris != "E":
    giris = input("Devam (E=çık): ")
    sayac += 1
print(f"{sayac} kez soruldu")
```

---

## BÖLÜM 8 — Fonksiyonlar

---

**S46. Fonksiyon neden kullanılır?**

**Cevap:**
- Aynı kodu defalarca yazmaktan kurtarır
- Kod daha kısa ve okunabilir
- Hata bulmak kolaylaşır
- Büyük programları yönetmek kolaylaşır

---

**S47. Python'da fonksiyon nasıl tanımlanır?**

**Cevap:**
```python
def fonksiyon_adi(parametre):
    # gövde
    return sonuç
```
- `def` → tanımlama başlar
- İsim → değişken kurallarına uymalı
- Parametre → parantez içinde (boş da olabilir)
- Gövde → girintili
- `return` → sonucu döndür

---

**S48. `return` komutu ne yapar?**

**Cevap:** Fonksiyonun hesapladığı değeri çağrıldığı yere gönderir ve fonksiyonu sonlandırır.
```python
def kare(n):
    return n * n

sonuc = kare(5)    # return → 25'i sonuc'a gönderir
print(sonuc)       # 25
```

---

**S49. Fonksiyon tanımlandıktan hemen sonra çalışır mı?**

**Cevap:** Hayır. Tanımlama sadece fonksiyonu hafızaya kaydeder. Ancak `fonksiyon_adi()` şeklinde çağrıldığında çalışır.

---

**S50. Parametresi olmayan fonksiyon yazılabilir mi?**

**Cevap:** Evet, parantezler boş bırakılır.
```python
def selam():
    print("Merhaba!")

selam()   # Merhaba!
```

---

**S51. Fonksiyon birden fazla kez çağrılabilir mi?**

**Cevap:** Evet, istenildiği kadar çağrılabilir.
```python
def kare(n):
    return n * n

print(kare(2))   # 4
print(kare(5))   # 25
print(kare(9))   # 81
```

---

**S52. Aşağıdaki kodun çıktısı nedir?**
```python
def topla(a, b):
    return a + b

x = topla(3, 7)
print(x)
```
**Cevap:** `10`

---

## BÖLÜM 9 — Karma / Kod Okuma

---

**S53. Aşağıdaki kodun çıktısı nedir?**
```python
for i in range(1, 4):
    print(i * i)
```
**Cevap:**
```
1
4
9
```

---

**S54. Aşağıdaki programda hata var mı? Varsa nedir?**
```python
sayi = input("Sayı: ")
sonuc = sayi * 2
print(sonuc)
```
**Cevap:** Mantık/tip hatası. `input()` string döner. `"5" * 2` → `"55"` (string iki kez tekrar). Doğrusu:
```python
sayi = int(input("Sayı: "))
sonuc = sayi * 2
```

---

**S55. Fahrenheit'ı Celsius'a çeviren program yazın. (Formül: C = (F - 32) × 5/9)**

**Cevap:**
```python
f = float(input("Fahrenheit: "))
c = (f - 32) * 5 / 9
print(f"Celsius: {round(c, 2)}")
```
*Not:* Hoca bu örneği derste anlattı — çalışma zamanı ve mantık hatabcığı konusunda.
