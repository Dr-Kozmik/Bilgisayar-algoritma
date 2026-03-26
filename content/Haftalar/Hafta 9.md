# Hafta 9 — while Döngüsü ve elif

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 8]] | Sonraki → [[Hafta 10-11]]

---

## while Döngüsü
```python
while koşul:
    # koşul True olduğu sürece çalışır
    komutlar
```

> ⚠️ Sayacı artırmayı unutursanız **sonsuz döngü** oluşur!

### Sayaç Örneği (Hocanın anlattığı)
```python
sayac = 1
while sayac <= 5:
    print(sayac)
    sayac += 1      # ZORUNLU! Unutma.
# Çıktı: 1 2 3 4 5
```

---

## for vs while

| | `for` | `while` |
|--|-------|---------|
| Kullanım | Sayısı belli tekrarlar | Koşula bağlı tekrarlar |
| `range()` | Gerekli | Gerekli değil |
| Sayaç artışı | Otomatik | **Manuel** |

---

## elif — Else If
```python
x = 15

if x < 0:
    print("Negatif")
elif x == 0:
    print("Sıfır")
elif x < 10:
    print("Küçük pozitif")
else:
    print("Büyük pozitif")
# → Büyük pozitif
```

---

## Klavyeden Çıkış Kontrolü (while + input)
```python
giris = "y"
sayac = 0
while giris != "H" and giris != "h":
    sayac += 1
    print(f"Tur: {sayac}")
    giris = input("Devam (Y) / Çık (H): ")
print(f"Toplam {sayac} tur döndü")
```

---

## Bağlantılı Konular
- [[Konular/Döngüler (for-while)]]
- [[Konular/Koşul Yapıları (if-elif-else)]]
- [[Hafta 10-11]] ← Fonksiyonlar
