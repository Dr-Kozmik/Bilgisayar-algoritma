# Hafta 7 — for Döngüsü

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 6]] | Sonraki → [[Hafta 8]]

---

## for Döngüsü Sözdizimi
```python
for değişken in range(başlangıç, bitiş, artım):
    # kod bloğu
```

---

## range() Fonksiyonu (Sınavda Çıkar!)

```python
range(5)          # 0, 1, 2, 3, 4      (5 dahil DEĞİL)
range(1, 6)       # 1, 2, 3, 4, 5      (6 dahil DEĞİL)
range(1, 11, 2)   # 1, 3, 5, 7, 9      (ikişer artış)
range(10, 0, -1)  # 10, 9, 8, ..., 1   (azalan)
```

> ⚠️ **Bitiş değeri dahil değildir!**  
> 10 kez dönmek için → `range(1, 11)` veya `range(10)`

---

## Örnekler

```python
# 1'den 10'a kadar
for i in range(1, 11):
    print(i)

# Çift sayılar (2, 4, 6, 8, 10)
for i in range(2, 11, 2):
    print(i)

# Geriye sayma
for i in range(5, 0, -1):
    print(i)

# Yanda yazdırma (end parametresi)
for i in range(1, 6):
    print(i, end=" ")    # 1 2 3 4 5
```

---

## Hocanın Örneği (Saniyeyi Saat/Dakika/Saniyeye Çevirme)
```python
saniye = int(input("Saniye giriniz: "))
saat = saniye // 3600
dakika = (saniye % 3600) // 60
kalan_sn = saniye % 60
print(saat, ":", dakika, ":", kalan_sn)
```

→ `//` ve `%` operatörleri için bak: [[Konular/Operatörler]]

---

## format() Metodu (Hocanın anlattığı)

> Hoca: "Format metodunu bilmek gerekiyor, çıktıyı düzgün biçimlendirmek için kullanılır."

```python
# Eski stil: .format()
print("{} {} yaşında".format("Ali", 20))
# → Ali 20 yaşında

# Birden fazla değer
print("{} {} seviyor".format("Ahmet", "futbolu"))

# Sıra numarası ile
print("{0} ve {1}".format("A", "B"))   # A ve B
print("{1} ve {0}".format("A", "B"))   # B ve A
```

> 💡 Yeni Python'da `f-string` daha pratik: `f"Ali {yas} yaşında"`  
> Ama hoca `format()` metodunu derste anlattı.

---

## Bağlantılı Konular
- [[Konular/Döngüler (for-while)]]
- [[Hafta 9]] ← while döngüsü
