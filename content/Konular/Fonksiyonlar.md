# Fonksiyonlar

🏠 [[🏠 Ana Sayfa]] | Kaynak: [[Haftalar/Hafta 10-11]]

---

## Tanım ve Çağırma

```python
# TANIMLAMA (bir kez yaz)
def fonksiyon_adi(parametre):
    # gövde
    return sonuç

# ÇAĞIRMA (istediğin kadar kullan)
sonuc = fonksiyon_adi(deger)
```

---

## Yapı Bileşenleri

| Bileşen | Açıklama | Örnek |
|---------|----------|-------|
| `def` | Fonksiyon tanımlanıyor | `def topla(a, b):` |
| **İsim** | Anlamlı isim ver | `topla`, `alan`, `kare_kok` |
| **Parametre** | Gelen veri | `(a, b)` |
| **Gövde** | Yapılacak işler (girintili) | `return a + b` |
| `return` | Sonucu geri döndür | `return sonuc` |

---

## Örnekler

### Parametresiz
```python
def merhaba():
    print("Merhaba Dünya!")

merhaba()   # Merhaba Dünya!
merhaba()   # Tekrar çağırılabilir!
```

### Parametreli + return
```python
def kare(n):
    return n * n

print(kare(4))   # 16
print(kare(7))   # 49
```

### Birden Fazla Parametre
```python
def topla(a, b):
    return a + b

sonuc = topla(3, 5)
print(sonuc)   # 8
```

### Gerçek Dünya Örneği (Hocanın gösterdiği)
```python
def alan(kenar):
    return kenar * kenar

# Bir kez tanımla, defalarca kullan
print(alan(3))   # 9
print(alan(5))   # 25
print(alan(7))   # 49
```

---

## Hazır Fonksiyonlar
```python
# Temel
abs(-5)          # 5
round(3.7, 0)    # 4.0
max(1, 5, 3)     # 5
min(1, 5, 3)     # 1
len("Merhaba")   # 7

# Math modülü
import math
math.sqrt(16)    # 4.0
math.pi          # 3.14159...
math.ceil(3.2)   # 4
math.floor(3.9)  # 3
```

---

## Önemli Notlar

> ⚠️ Fonksiyon tanımlandığı anda çalışmaz — çağrıldığında devreye girer.

> ⚠️ `return` olmayan fonksiyon `None` döndürür.

> 💡 AI Notu: Parametreye varsayılan değer verebilirsiniz: `def f(x=10):` → `f()` çağırırsanız x=10 olur.
