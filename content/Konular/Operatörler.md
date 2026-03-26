# Operatörler

🏠 [[🏠 Ana Sayfa]] | Kaynak: [[Haftalar/Hafta 4]] · [[Haftalar/Hafta 5]] · [[Haftalar/Hafta 6]]

---

## Aritmetik Operatörler

| Operatör | İşlem | Örnek | Sonuç |
|----------|-------|-------|-------|
| `+` | Toplama | `5 + 3` | `8` |
| `-` | Çıkarma | `5 - 3` | `2` |
| `*` | Çarpma | `5 * 3` | `15` |
| `/` | Bölme | `5 / 2` | `2.5` |
| `//` | **Tam Bölme** | `5 // 2` | `2` |
| `%` | **Modulo (Kalan)** | `5 % 2` | `1` |
| `**` | Üs alma | `2 ** 3` | `8` |

> **`//` nedir?** Bölme işleminin **tam sayı** kısmını verir.  
> **`%` nedir?** Bölme işleminin **kalanını** verir.

### `//` ve `%` Kullanım Örneği (Saniye → Saat/Dakika)
```python
saniye = 7261
saat   = saniye // 3600        # 2
dakika = (saniye % 3600) // 60 # 0
kalan  = saniye % 60           # 1
```

---

## Öncelik Sırası (Sınavda Çıkar!)
```
1. ()   Parantez        → en yüksek öncelik
2. **   Üs alma
3. * / // %  Çarp/Böl
4. + -  Topla/Çıkar    → en düşük öncelik
```

**Örnek:**
```python
2 + 3 * 4       # = 14  (önce çarpma)
(2 + 3) * 4     # = 20  (önce parantez)
```

---

## Karşılaştırma Operatörleri

| `==` | `!=` | `>` | `<` | `>=` | `<=` |
|------|------|-----|-----|------|------|
| Eşit mi? | Farklı mı? | Büyük mü? | Küçük mü? | Büyük eşit? | Küçük eşit? |

> ⚠️ `=` atama, `==` karşılaştırma!

---

## Mantıksal Operatörler

→ Detay: [[Koşul Yapıları (if-elif-else)]]

```python
and   # İkisi de True → True
or    # Biri True → True
not   # Tersini al
```

---

## Kısaltmalı Atama Operatörleri
```python
x += 5   # x = x + 5
x -= 3   # x = x - 3
x *= 2   # x = x * 2
x /= 4   # x = x / 4
x //= 2  # x = x // 2
x %= 3   # x = x % 3
```
