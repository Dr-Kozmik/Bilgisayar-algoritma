# Hafta 8 — Uygulama Örnekleri ve String İşlemleri

🏠 [[🏠 Ana Sayfa]] | ← [[Hafta 7]] | Sonraki → [[Hafta 9]]

---

## String Birleştirme (+)
```python
isim = input("İsminizi giriniz: ")
print("Merhaba " + isim)

# Sayıyı metinle birleştirmek için str() gerekir
yas = 20
print("Yaşınız: " + str(yas))
```

## f-string (Formatlı Yazdırma)
```python
ad = "Ali"
yas = 20
print(f"Merhaba {ad}, yaşınız {yas}")
# → Merhaba Ali, yaşınız 20
```

---

## Hocanın Uygulama Örnekleri

### İki Sayı Toplamı
```python
sayi1 = float(input("Birinci sayı: "))
sayi2 = float(input("İkinci sayı: "))
toplam = sayi1 + sayi2
print(f"Toplam: {toplam}")
```

### Ortalama Hesaplama
```python
sayi1 = float(input("Birinci sayı: "))
sayi2 = float(input("İkinci sayı: "))
ortalama = (sayi1 + sayi2) / 2
print(f"Ortalama: {ortalama}")
```

> Hoca özel vurgu: **Kendi değişikliklerinizi de ekleyin** — "aynısını yazmak öğretmez, bir şeyler değiştirin."

---

## float vs int Ne Zaman Kullanılır?
- Kullanıcı virgüllü sayı girebilecekse → `float(input(...))`
- Kesinlikle tam sayı ise → `int(input(...))`

---

## Bağlantılı Konular
- [[Konular/Değişkenler ve Veri Tipleri]]
- [[Hafta 9]] ← while döngüsü
