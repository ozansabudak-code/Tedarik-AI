# Tedarik-AI

## Tedarikçi Rapor Analiz Sistemi

Kapsamlı tedarikçi performans yönetimi, analiz ve uyumluluk takip sistemi.

## Yeni Özellik: Cari Bilgi Kayıt ve Mail Paneli

Tedarikçi Uyumluluk Merkezi'ne eklenen yeni özellik ile:

### ✨ Özellikler

1. **Cari Bilgi Giriş Ekranı:**
   - Tedarikçi adı, yetkili kişi, telefon, adres bilgileri
   - Alım türü seçimi (Kumaş, Fire, Tekleme, Aksesuar, Diğer)
   - Mail adresi
   - Eksik evrak takibi (Sözleşme, Sertifika, Vergi Levhası, vb.)

2. **Excel Entegrasyonu:**
   - Otomatik Excel dosyası oluşturma
   - Kayıtlar: `X:\01.Public\TEDARİKÇİ PERFORMANS\Cari Bilgiler\Cari Bilgiler.xlsx`
   - Mevcut kayıtları otomatik listeleme
   - Excel'den doğrudan veri okuma

3. **Mail Yönetimi:**
   - Tekli mail gönderimi
   - Toplu mail gönderimi
   - Mail şablonları:
     - Evrak Eksikliği Bildirimi
     - Sözleşme Yenileme Hatırlatması
     - Sertifika Güncellemesi
     - Genel Bilgilendirme
   - Otomatik mail kişiselleştirme

4. **Evrak Takibi:**
   - Eksik evrak işaretleme
   - Filtre ve arama özellikleri
   - Alım türüne göre filtreleme

### 🚀 Kullanım

1. **Tedarikçi Uyumluluk Merkezi** sekmesine gidin
2. **Cari Bilgiler Kayıt ve Mail Paneli** bölümünü bulun
3. Yeni tedarikçi eklemek için formu doldurun ve **Kaydet** butonuna tıklayın
4. Kayıtlı tedarikçilere mail göndermek için:
   - Mail şablonu seçin
   - Konu ve içeriği düzenleyin
   - Listeden tedarikçi(ler) seçin
   - **Seçili Tedarikçilere Gönder** veya **Toplu Mail Gönder** butonuna tıklayın

### 📋 Gereksinimler

- Python 3.x
- openpyxl (Excel işlemleri için)
- pandas
- tkinter / customtkinter
- Diğer bağımlılıklar (mevcut requirements'ta)

### 🔧 Kurulum

```bash
pip install openpyxl pandas
```

### 📝 Not

- Excel dosyası otomatik olarak oluşturulur
- Mail gönderimleri Gmail SMTP kullanır
- Tüm aktiviteler sistem loglarına kaydedilir