# Koşul Yapıları (if-elif-else)

🏠 [[🏠 Ana Sayfa]] | Kaynak: [[Haftalar/Hafta 5]] · [[Haftalar/Hafta 6]] · [[Haftalar/Hafta 9]]

---

## Temel Yapı
```python
if koşul:
    # koşul True ise
elif başka_koşul:
    # ilk koşul False, bu True ise
else:
    # hepsi False ise
```

### Kurallar
- Her `if`/`elif`/`else` sonrasına `:` zorunlu
- İçerideki kod **4 boşluk** girintili
- `elif` ve `else` isteğe bağlıdır

---

## if-else Örneği
```python
sayi = int(input("Sayı: "))
if sayi > 0:
    print("Pozitif")
else:
    print("Sıfır veya negatif")
```

## if-elif-else Örneği
```python
not_puan = int(input("Not: "))
if not_puan >= 90:
    print("AA")
elif not_puan >= 80:
    print("BA")
elif not_puan >= 70:
    print("BB")
elif not_puan >= 60:
    print("CB")
else:
    print("Kaldı")
```

---

## Mantıksal Operatörler ile Birleşik Koşul

```python
yas = int(input("Yaş: "))

# and — ikisi de sağlanmalı
if yas >= 18 and yas <= 65:
    print("Çalışabilir")

# or — biri yeterli
if yas < 0 or yas > 150:
    print("Geçersiz yaş")

# not — tersini al
if not (yas >= 18):
    print("Reşit değil")
```

### Doğruluk Tablosu (Ezbere!)

| A | B | A and B | A or B |
|---|---|---------|--------|
| T | T | **T** | **T** |
| T | F | **F** | **T** |
| F | T | **F** | **T** |
| F | F | **F** | **F** |

---

## pass İfadesi
```python
if x > 0:
    pass   # Şimdilik bir şey yapma
else:
    print("Negatif")
```

---

## İç İçe if
```python
if x > 0:
    if x % 2 == 0:
        print("Pozitif çift")
    else:
        print("Pozitif tek")
```
