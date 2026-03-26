# Hafta 5 — Hata Türleri, if-else ve Boolean

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 4]] | Sonraki → [[Hafta 6]]

---

## Boolean (bool) Tipi
```python
True    # Doğru = 1
False   # Yanlış = 0
```

## Karşılaştırma Operatörleri

| Operatör | Anlamı | Örnek | Sonuç |
|----------|--------|-------|-------|
| `==` | Eşit mi? | `5 == 5` | `True` |
| `!=` | Farklı mı? | `5 != 3` | `True` |
| `>` | Büyük mü? | `5 > 3` | `True` |
| `<` | Küçük mü? | `3 < 5` | `True` |
| `>=` | Büyük eşit? | `5 >= 5` | `True` |
| `<=` | Küçük eşit? | `3 <= 5` | `True` |

> ⚠️ `=` atama, `==` karşılaştırmadır! Karıştırmayın.

---

## if-else Yapısı
```python
if koşul:
    # True ise çalışır
    ...
else:
    # False ise çalışır
    ...
```

**Hocanın örneği (sıfıra bölme kontrolü):**
```python
bolen = int(input("Bölen: "))
if bolen != 0:
    bolum = int(input("Bölünen: "))
    print("Sonuç:", bolum / bolen)
else:
    print("Sıfıra bölme yapılamaz!")
```

---

## Girintileme — Kritik!
- Python'da girinti **sözdizimsel** anlam taşır (süslü parantez yok!)
- `if`, `else`, `for`, `while`, `def` altındaki kod **4 boşluk** içeri girer
- Hatalı girinti → `IndentationError`

---

## Yorumlar (#)
```python
# Bu satır çalışmaz
x = 5  # satır sonu yorumu
```

---

## Bağlantılı Konular
- [[Konular/Hata Türleri]] ← 3 hata türünün detayı
- [[Konular/Koşul Yapıları (if-elif-else)]]
- [[Hafta 6]] ← and, or, not
