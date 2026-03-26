# Hafta 4 — Değişkenler, Veri Tipleri ve Operatörler

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 3]] | Sonraki → [[Hafta 5]]

---

## Veri Tipleri

| Tip | Örnek | Açıklama |
|-----|-------|----------|
| `int` | `x = 5` | Tam sayı |
| `float` | `x = 3.14` | Ondalıklı sayı |
| `str` | `x = "Ali"` | Metin |
| `bool` | `x = True` | Doğru/Yanlış |

→ Detay: [[Konular/Değişkenler ve Veri Tipleri]]

---

## Değişken Kuralları (Sınavda Çıkar!)
- ✅ Harf veya `_` ile başlamalı: `ad`, `_toplam`, `sayi1`
- ❌ Rakamla başlamaz: `1sayi`
- ❌ Boşluk içeremez: `benim sayi`
- ❌ Özel karakter yok: `#ad`, `@x`
- ❌ Anahtar kelimeler kullanılamaz: `if`, `for`, `while`...
- 🔤 Büyük/küçük harf farkı: `Ad ≠ ad`

---

## del Komutu
```python
x = 10
del x       # x bellekten silindi
print(x)    # NameError!
```

---

## Çoklu Atama
```python
a = b = c = 0
x, y, z = 1, 2, 3
```

---

## Özel Fonksiyonlar
```python
type(x)          # Tipi öğren → <class 'int'>
int("42")        # Metni sayıya
float("3.14")    # Metni ondalığa
str(100)         # Sayıyı metne
round(3.567, 2)  # → 3.57 (2 basamak)
```

---

## Operatörler

→ Detay: [[Konular/Operatörler]]

**Hızlı özet:**
```
+  Top  |  -  Çık  |  *  Çarp  |  /  Böl
//  Tam böl  |  %  Kalan  |  **  Üs
```

**Kısaltmalı atama:**
```python
x += 5   # x = x + 5
x -= 3   # x = x - 3
x *= 2   # x = x * 2
```

**Öncelik sırası:** `()` → `**` → `* / // %` → `+ -`

---

## Bağlantılı Konular
- [[Konular/Operatörler]]
- [[Konular/Değişkenler ve Veri Tipleri]]
- [[Hafta 5]] ← if-else
