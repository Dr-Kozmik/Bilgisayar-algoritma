# Hata Türleri

🏠 [[🏠 Ana Sayfa]] | Kaynak: [[Haftalar/Hafta 1-2]] · [[Haftalar/Hafta 5]]

---

## 3 Hata Türü (Sınavda Çıkar!)

### 1. Söz Dizimi Hatası (Syntax Error)
- **Ne zaman?** Program çalışmadan önce, çeviri aşamasında
- **Kim bulur?** Yorumlayıcı otomatik bulur ve satır numarası söyler
- **Örnekler:**
  - Parantez açıp kapatmamak: `print("Merhaba"`
  - Yanlış operatör kullanımı
  - Hatalı girinti
  - `if` sonrasına `:` koymamak

### 2. Çalışma Zamanı Hatası (Runtime Error)
- **Ne zaman?** Program çalışmaya başladıktan sonra, çalışırken
- **Kim bulur?** Yorumlayıcı tarafında çalışma sırasında yakalanır
- **Örnekler:**
  ```python
  x = int(input())  # Kullanıcı "abc" girerse → ValueError
  y = 5 / 0         # Sıfıra bölme → ZeroDivisionError
  print(z)          # z tanımlanmamış → NameError
  ```

### 3. Mantık Hatası (Logic Error)
- **Ne zaman?** Her zaman — program çalışır ama **yanlış sonuç** verir
- **Kim bulur?** **Yorumlayıcı BULAMAZ** — sadece programcı fark edebilir
- **Örnekler:**
  ```python
  # Sıcaklık formülü yanlış yazılmış
  derecec = (9/5) * fahrenheit - 32   # YANLIŞ
  derecec = (fahrenheit - 32) * 5/9  # DOĞRU
  ```

> 🔴 Hoca vurgusu: "Mantık hataları en zor bulunan hata türüdür. Yorumlayıcı hiçbir yardımda bulunamaz."

---

## Karşılaştırma Tablosu

| | Söz Dizimi | Çalışma Zamanı | Mantık |
|-|-----------|----------------|--------|
| **Ne zaman?** | Çalışmadan önce | Çalışırken | Her zaman |
| **Yorumlayıcı bulur mu?** | ✅ Evet | ✅ Evet | ❌ Hayır |
| **Program çalışır mı?** | ❌ Hayır | Başlar, durur | ✅ Evet (yanlış) |
