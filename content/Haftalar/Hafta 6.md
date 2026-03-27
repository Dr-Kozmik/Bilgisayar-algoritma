# Hafta 6 — Mantıksal Operatörler ve Koşul Yapıları

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 5]] | Sonraki → [[Hafta 7]]

---

## Mantıksal Operatörler (Sınavda Çıkar!)

| Operatör | Anlamı | Kural |
|----------|--------|-------|
| `and` | VE | İkisi de True → True |
| `or` | VEYA | Biri True → True |
| `not` | DEĞİL | True→False, False→True |

### Doğruluk Tablosu

| E1 | E2 | E1 and E2 | E1 or E2 | not E1 |
|----|----|-----------|----------|--------|
| True | True | **True** | **True** | False |
| True | False | **False** | **True** | False |
| False | True | **False** | **True** | True |
| False | False | **False** | **False** | True |

> 🔴 Hoca vurguladı: "Bu tabloyu bilmeniz şart, sınavda mutlaka sorarım."

### Örnekler
```python
x, y = 10, 20

if x == 10 and y == 20:
    print("İkisi de doğru")   # ✅ çalışır

if x == 5 or y == 20:
    print("En az biri doğru") # ✅ çalışır

if not (x == 5):
    print("x, 5 değil")       # ✅ çalışır
```

---

## İç İçe if (Nested if)
```python
if koşul1:
    if koşul2:
        print("İkisi de doğru")
    else:
        print("Sadece 1. doğru")
else:
    print("1. doğru değil")
```

---

## pass İfadesi
```python
# Şimdilik bir şey yapma, devam et
if x > 0:
    pass
else:
    print("Negatif")
```

---

## ⚠️ Float Eşitlik Sorunu (Kayan Nokta Hassasiyeti)

> Hoca bu konuya Hafta 6'da değindi: "Bilgisayar ikilik sistemde çalıştığı için bazı ondalıklı sayı karşılaştırmaları beklenmedik sonuç verebilir."

```python
# Beklenti: True ama sonuç False!
print(0.1 + 0.2 == 0.3)    # False ❌

# Neden?
print(0.1 + 0.2)            # 0.30000000000000004

# Çözüm: round() ile karşılaştır
print(round(0.1 + 0.2, 1) == 0.3)   # True ✅
```

> 💡 Sınavda çıkma olasılığı düşük ama hocanın bahsettiği bir konu.

---

## Bağlantılı Konular
- [[Konular/Koşul Yapıları (if-elif-else)]]
- [[Hafta 7]] ← for döngüsü
