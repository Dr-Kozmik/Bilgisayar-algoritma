# Hafta 3 — Python'a Giriş ve IDE

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 1-2]] | Sonraki → [[Hafta 4]]

---

## IDE Seçenekleri
| IDE | Özellik |
|-----|---------|
| **Replit** | Tarayıcıda, kurulum yok |
| **PyCharm** | Profesyonel, renk kodlaması, hata uyarıları |
| **IDLE** | Python ile birlikte gelir |
| **VS Code** | Hocanın kullandığı |

---

## print() Fonksiyonu
```python
print("Merhaba Dünya")

# Birden fazla değer (virgülle)
print("Ad:", "Ali", "Yaş:", 20)

# Özel parametreler
print("A", "B", sep="-")     # → A-B
print("Merhaba", end=" ")    # satır sonu değiştir
print("Dünya")               # → Merhaba Dünya
```

> ⚠️ **sep** ve **end** parametreleri sınavda sorulabilir!  
> Varsayılan: `sep=" "` (boşluk), `end="\n"` (alt satır)

---

## input() Fonksiyonu
```python
ad = input("Adınız: ")
print("Merhaba", ad)
```

> ⚠️ `input()` her zaman **string** döner!  
> Sayısal işlem için dönüştürün: `int(input("Sayı: "))`

---

## Bağlantılı Konular
- [[Konular/Değişkenler ve Veri Tipleri]]
- [[Hafta 4]] ← Veri tipleri detayı
