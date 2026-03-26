# Hafta 10-11 — Fonksiyonlar

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 9]]

---

## Neden Fonksiyon?
- Aynı işlemi **defalarca yazmak** yerine bir kere tanımla, istediğin yerde çağır.
- Kod daha kısa, okunabilir ve hata bulmak kolay.

> Hoca benzetmesi: "Bina inşaatında her kat için aynı ekibi sıfırdan eğitmek yerine, bir kez eğit ve her kata gelince çağır."

---

## Hazır (Built-in) Fonksiyonlar
```python
abs(-5)          # 5
round(3.567, 2)  # 3.57
max(3, 7, 2)     # 7
min(3, 7, 2)     # 2
pow(2, 3)        # 8

import math
math.sqrt(25)    # 5.0
math.pi          # 3.14159...
```

---

## Kendi Fonksiyonunu Yazma

```python
def fonksiyon_adi(parametre1, parametre2):
    # gövde
    return sonuç
```

**4 bileşen:**
1. `def` — Fonksiyon tanımlanıyor
2. **İsim** — Anlamlı bir isim ver (değişken kuralları geçerli)
3. **Parametreler** — Fonksiyona gönderilecek veriler `()`nin içine
4. **Gövde** — Yapılacak işler (girintili)

---

## Örnekler

### Basit Örnek (Hocanın gösterdiği)
```python
def cift_yap(n):
    return n * 2

x = cift_yap(3)
print(x)    # 6
```

### Alan Hesaplama
```python
def alan(a):
    return a * a

print(alan(5))   # 25
print(alan(3))   # 9
print(alan(7))   # 49
# Bir kez yaz, defalarca kullan!
```

### Parametresiz Fonksiyon
```python
def sayi_say():
    for i in range(1, 11):
        print(i, end=" ")

sayi_say()   # 1 2 3 4 5 6 7 8 9 10
sayi_say()   # tekrar çağırabilirsin
```

---

## return Komutu
- Fonksiyonun hesapladığı değeri **geri döndürür**
- `return` olmadan fonksiyon `None` döner

```python
def topla(a, b):
    return a + b

sonuc = topla(3, 5)   # sonuc = 8
```

---

## Önemli Not
> Fonksiyon tanımlandığı anda **çalışmaz** — bir kenarda bekler.  
> `fonksiyon_adi()` ile çağrıldığında devreye girer.

---

## Bağlantılı Konular
- [[Konular/Fonksiyonlar]]
- [[Sınav/Sınav Soruları]]
