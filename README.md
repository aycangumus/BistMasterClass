# BistMasterClass

## BIST Formasyon Tarama ve Alarm Sistemi (Pine Script)

`indicators/formasyon-tarama-alarm.pine` — TradingView için Pine Script v6 indikatörü.
Grafikteki sembol üzerinde otomatik formasyon tespiti/çizimi yapar ve 10 adede kadar
ek BIST sembolünü aynı anda tarayarak sağ üstte bir tarama tablosu gösterir.

### Özellikler

- **Formasyon tespiti** (pivot tabanlı üst/alt trend çizgileri ile):
  Dikdörtgen, Simetrik Üçgen, Yükselen Üçgen, Alçalan Üçgen,
  Yükselen Kama, Düşen Kama, Yükselen Kanal, Düşen Kanal
- **Grafik çizimi**: formasyon çizgileri, gölgeli dolgu, formasyon adı etiketi ve
  kırılım etiketleri (▲ Yukarı Kırılım, ▼ Aşağı Kırılım, Trend Kırılımı/Fitil)
- **Tarama tablosu** sütunları:
  `SEM | FİYAT | YAPI | DURUM | SEVİYE | MESAFE % | HEDEF/KARŞI | SKOR | HACİM`
- **Durumlar**: ALT DESTEĞE GELDİ, ÜST KIRILIMA YAKIN, ÜST/ALT ÇİZGİYİ FİTİL KIRDI,
  SON BAR YUKARI/AŞAĞI KIRILIM • CANLI, FORMASYON İÇİNDE
- **HEDEF/KARŞI**: formasyon yüksekliğinin kırılım yönünde projeksiyonu
- **SKOR**: daralma (sıkışma), hacim ve seviyeye yakınlık bileşenlerinden 0–100 arası puan
- **HACİM**: son bar hacmi ortalamanın üzerindeyse ✓
- **RSI Uyumsuzluk**: grafik sembolü için pozitif/negatif uyumsuzluk kontrolü (tablo alt satırı)
- **Alarm**: durum değişimlerinde (desteğe geliş, fitil kırılımı, yukarı/aşağı kırılım)
  otomatik alarm mesajı üretir

### Kurulum

1. TradingView'da **Pine Editor**'ü açın.
2. `indicators/formasyon-tarama-alarm.pine` dosyasının içeriğini yapıştırın.
3. **Kaydet** ve **Grafiğe ekle** deyin.

### Alarm Kurulumu

1. TradingView'da **Alarm oluştur** penceresini açın.
2. Koşul olarak **Formasyon Tarama** indikatörünü seçin.
3. **"Any alert() function call"** seçeneğini seçip alarmı kaydedin.
4. Tablodaki tüm semboller için tek alarm yeterlidir; mesajda sembol, formasyon,
   durum ve fiyat yer alır.

### Ayarlar

- **Pivot Uzunluğu**: tepe/dip hassasiyeti (küçük değer = daha sık formasyon)
- **Yatay Eğim Eşiği**: çizginin "yatay" sayılacağı eğim sınırı (%/bar)
- **Daralma Oranı**: üçgen/kama ile kanal ayrımı için genişlik oranı
- **Destek/Direnç Yakınlık %**: "YAKIN/GELDİ" durumları için mesafe eşiği
- **Tarama Sembolleri**: 10 sembolü dilediğiniz BIST hisseleriyle değiştirebilirsiniz

> Not: Eğitim amaçlıdır; yatırım tavsiyesi değildir.
