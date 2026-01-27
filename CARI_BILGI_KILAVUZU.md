# Cari Bilgi Kayıt ve Mail Paneli - Kullanım Kılavuzu

## İçindekiler
1. [Genel Bakış](#genel-bakış)
2. [Özellikler](#özellikler)
3. [Kurulum](#kurulum)
4. [Kullanım](#kullanım)
5. [Mail Şablonları](#mail-şablonları)
6. [Sık Sorulan Sorular](#sık-sorulan-sorular)

---

## Genel Bakış

Cari Bilgi Kayıt ve Mail Paneli, tedarikçilerin iletişim bilgilerini merkezi bir sistemde yönetmenizi ve toplu veya tekil mail gönderimi yapmanızı sağlayan bir modüldür.

### Nerede Bulunur?

**Tedarikçi Uyumluluk Merkezi** → **Cari Bilgiler Kayıt ve Mail Paneli**

---

## Özellikler

### 📝 1. Cari Bilgi Girişi

Yeni tedarikçi bilgilerini sisteme ekleyebilirsiniz:

- **Tedarikçi Adı**: Firma adı (Zorunlu)
- **Yetkili Kişi**: İletişim kurulacak kişi
- **Telefon**: İletişim telefonu
- **Mail**: E-posta adresi (Zorunlu)
- **Adres**: Firma adresi
- **Alım Türü**: Kumaş, Fire, Tekleme, Aksesuar, Diğer
- **Eksik Evraklar**: İşaretlenebilir evrak listesi
  - Sözleşme
  - Sertifika
  - Vergi Levhası
  - İmza Sirküleri
  - Fatura Bilgileri

### 📊 2. Kayıt Listeleme

Tüm kayıtlı tedarikçiler bir tabloda görüntülenir:

- **Sütunlar**: Tedarikçi, Yetkili, Telefon, Mail, Alım Türü, Eksik Evraklar, Tarih
- **Arama**: Tedarikçi adı veya yetkili kişiye göre arama
- **Filtreleme**: Alım türüne göre filtreleme
- **Yenileme**: Liste yenileme butonu

### 📧 3. Mail Gönderimi

İki farklı mail gönderim seçeneği:

#### A. Tekli Mail Gönderimi
1. Listeden bir veya birden fazla tedarikçi seçin
2. Mail şablonu seçin
3. Konu ve içeriği düzenleyin
4. **"Seçili Tedarikçilere Gönder"** butonuna tıklayın

#### B. Toplu Mail Gönderimi
1. Mail şablonu seçin
2. Konu ve içeriği düzenleyin
3. **"Toplu Mail Gönder (Tüm Liste)"** butonuna tıklayın
4. Onay mesajını kabul edin

### 🔍 4. Arama ve Filtreleme

- **Arama Kutusu**: Tedarikçi veya yetkili kişi adına göre arama
- **Alım Türü Filtresi**: Belirli bir alım türüne göre filtreleme
- **Temizle Butonu (🔄)**: Tüm filtreleri sıfırla

---

## Kurulum

### Gereksinimler

```bash
pip install openpyxl pandas
```

### Excel Dosyası

Excel dosyası otomatik olarak şu konumda oluşturulur:
```
X:\01.Public\TEDARİKÇİ PERFORMANS\Cari Bilgiler\Cari Bilgiler.xlsx
```

> **Not**: İlk kullanımda klasör yoksa otomatik oluşturulur.

---

## Kullanım

### Yeni Tedarikçi Ekleme

1. **Formu Doldurun**:
   - Tedarikçi adını girin (zorunlu)
   - Mail adresini girin (zorunlu)
   - Diğer bilgileri tamamlayın
   - Eksik evrakları işaretleyin

2. **Kaydet**:
   - 💾 **Kaydet** butonuna tıklayın
   - Başarılı mesajı gelecek
   - Form otomatik temizlenecek
   - Liste güncellenecek

3. **Formu Temizle**:
   - 🔄 **Temizle** butonu tüm alanları sıfırlar

### Mail Gönderme

#### Adım 1: Şablon Seçimi

Açılır menüden bir şablon seçin:
- Evrak Eksikliği Bildirimi
- Sözleşme Yenileme Hatırlatması
- Sertifika Güncellemesi
- Genel Bilgilendirme

Şablon seçildiğinde konu ve içerik otomatik dolar.

#### Adım 2: İçeriği Düzenleme

Mail konusunu ve içeriğini ihtiyaca göre düzenleyin.

**Kullanılabilir Değişkenler** (otomatik değiştirilir):
- `{{Tedarikçi Adı}}` → Tedarikçinin adı
- `{{Yetkili Kişi}}` → Yetkili kişinin adı
- `{{Eksik Evraklar}}` → Eksik evrak listesi

Örnek:
```
Sayın {{Yetkili Kişi}},

{{Tedarikçi Adı}} firması için bazı evrakların eksik olduğunu tespit ettik.

Eksik Evraklar:
{{Eksik Evraklar}}
```

#### Adım 3: Alıcı Seçimi

**Tekli Mail için**:
- Listeden bir veya birden fazla satır seçin (Ctrl+tıkla)

**Toplu Mail için**:
- Tüm listeye gönderilir
- Aktif filtreler dikkate alınır

#### Adım 4: Gönderim

- 📧 **Seçili Tedarikçilere Gönder**: Seçili kayıtlara gönder
- 📧 **Toplu Mail Gönder**: Tüm listeye gönder

**Sonuç**:
- Başarılı mail sayısı gösterilir
- Başarısız olanlar raporlanır
- Tüm gönderimler aktivite loguna kaydedilir

### Excel Dosyasını Açma

📋 **Excel'i Aç** butonuna tıklayarak dosyayı doğrudan açabilirsiniz.

---

## Mail Şablonları

### 1. Evrak Eksikliği Bildirimi

**Konu**: Tedarikçi Evrak Eksikliği Bildirimi

**Kullanım**: Tedarikçinin eksik evraklarını bildirmek için

**İçerik Değişkenleri**:
- {{Tedarikçi Adı}}
- {{Yetkili Kişi}}
- {{Eksik Evraklar}}

---

### 2. Sözleşme Yenileme Hatırlatması

**Konu**: Sözleşme Yenileme Hatırlatması

**Kullanım**: Sözleşme yenileme zamanı yaklaşan tedarikçilere

**İçerik Değişkenleri**:
- {{Tedarikçi Adı}}
- {{Yetkili Kişi}}

---

### 3. Sertifika Güncellemesi

**Konu**: Sertifika Güncelleme Talebi

**Kullanım**: Sertifikaları güncellemesi gereken tedarikçilere

**İçerik Değişkenleri**:
- {{Tedarikçi Adı}}
- {{Yetkili Kişi}}

---

### 4. Genel Bilgilendirme

**Konu**: Genel Bilgilendirme

**Kullanım**: Özel mesajlar için

**İçerik**: Tamamen özelleştirilebilir

---

## Sık Sorulan Sorular

### S: Excel dosyası nerede oluşturuluyor?

**C**: `X:\01.Public\TEDARİKÇİ PERFORMANS\Cari Bilgiler\Cari Bilgiler.xlsx`

İlk kullanımda klasör ve dosya otomatik oluşturulur.

---

### S: Mail gönderemedim, ne yapmalıyım?

**C**: Kontrol edilmesi gerekenler:
1. Gmail SMTP ayarlarının doğru olduğundan emin olun
2. İnternet bağlantınızı kontrol edin
3. Mail adresinin doğru girildiğinden emin olun
4. Uygulama loglarını kontrol edin

---

### S: Toplu mail gönderirken filtre çalışıyor mu?

**C**: Evet! Arama ve filtreleme aktifse, sadece görüntülenen kayıtlara mail gönderilir.

---

### S: Mail içeriğindeki değişkenler nasıl çalışıyor?

**C**: `{{Değişken Adı}}` formatındaki tüm değişkenler, her tedarikçi için otomatik olarak o tedarikçinin bilgileriyle değiştirilir.

Desteklenen değişkenler:
- `{{Tedarikçi Adı}}`
- `{{Yetkili Kişi}}`
- `{{Eksik Evraklar}}`

---

### S: Excel dosyasını manuel olarak düzenleyebilir miyim?

**C**: Evet! Excel'i açarak manuel düzenleme yapabilirsiniz. Ancak:
- Başlık satırını değiştirmeyin
- Sütun sırasını değiştirmeyin
- Uygulama kapalıyken düzenleme yapın

Değişiklikler sonrası uygulamada **🔄 Listeyi Yenile** butonuna tıklayın.

---

### S: Kayıtları silebilir miyim?

**C**: Şu anda UI'dan silme özelliği yok. Excel dosyasını açıp manuel olarak satırları silebilirsiniz.

---

### S: Mail gönderimi loglanıyor mu?

**C**: Evet! Tüm mail gönderimler ActivityLogger tarafından kaydedilir ve günlük raporlarda görüntülenebilir.

---

## Destek

Sorun veya önerileriniz için:
- Issue açın: [GitHub Issues](https://github.com/ozansabudak-code/Tedarik-AI/issues)
- Mail: ozan.sabudak@defacto.com

---

## Güncelleme Geçmişi

**v2.8** (Ocak 2026)
- ✅ Cari Bilgi Kayıt ve Mail Paneli eklendi
- ✅ Excel entegrasyonu
- ✅ Mail şablonları sistemi
- ✅ Toplu mail gönderimi
- ✅ Evrak takip sistemi

---

*Son Güncelleme: Ocak 2026*
