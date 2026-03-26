# Değişkenler ve Veri Tipleri

🏠 [[🏠 Ana Sayfa]] | Kaynak: [[Haftalar/Hafta 3]] · [[Haftalar/Hafta 4]]

---

## Veri Tipleri

| Tip | Örnek | Açıklama |
|-----|-------|----------|
| `int` | `x = 5` | Tam sayı |
| `float` | `x = 3.14` | Ondalıklı sayı |
| `str` | `x = "Ali"` | Metin (tırnak içinde) |
| `bool` | `x = True` | Doğru (`True`) / Yanlış (`False`) |

```python
type(5)      # <class 'int'>
type(3.14)   # <class 'float'>
type("Ali")  # <class 'str'>
type(True)   # <class 'bool'>
```

---

## Tip Dönüşümleri (Type Casting)

```python
int("42")        # "42" → 42
int(3.9)         # 3.9 → 3  (kesir kısmı atılır!)
float("3.14")    # "3.14" → 3.14
float(5)         # 5 → 5.0
str(100)         # 100 → "100"
str(3.14)        # 3.14 → "3.14"
bool(0)          # 0 → False
bool(1)          # 1 → True
```

> ⚠️ `input()` her zaman **str** döner!
> ```python
> x = input("Sayı: ")   # x = "5" (string!)
> x = int(input("Sayı: "))  # x = 5  (int ✅)
> ```

---

## Değişken Kuralları (Sınavda Çıkar!)

| ✅ Geçerli | ❌ Geçersiz |
|-----------|-----------|
| `sayi` | `1sayi` (rakamla başlıyor) |
| `_ad` | `benim ad` (boşluk var) |
| `toplam1` | `#toplam` (özel karakter) |
| `ogrenci_adi` | `if` (anahtar kelime) |

- **Büyük/küçük harf farkı:** `Ad ≠ ad ≠ AD`

---

## Özel Komutlar
```python
del x         # x değişkenini bellekten sil
round(3.56, 1)  # → 3.6  (1 ondalık basamak)

# Çoklu atama
a = b = c = 0
x, y, z = 1, 2, 3
```

---

## Hafızadaki Davranış
- Bir değişkene yeni değer atandığında, eski değer silinir
- `del` ile değişken tamamen bellekten silinir, erişmeye kalkarsanız `NameError`
