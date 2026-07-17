# 🧠 MR Okuma Atölyesi — DICOM Görüntüleyici & Öğretici

Tıp öğrencileri için **tarayıcıda çalışan**, kurulum gerektirmeyen bir DICOM MR
görüntüleyici ve adım adım okuma öğreticisi. Tek bir `index.html` dosyasıdır;
harici hiçbir kütüphaneye veya sunucuya ihtiyaç duymaz. Tüm veriler yalnızca
senin cihazında işlenir — hiçbir dosya internete gönderilmez.

> ⚠️ **Sadece eğitim amaçlıdır. Tanı için kullanılamaz.** Gerçek radyolojik
> değerlendirme, kalibre monitörlerde ve hekim denetiminde yapılır.

## Ne yapar?

- **Kendi Hasta CD'ndeki DICOM dosyalarını açar** (sıkıştırılmamış Explicit/Implicit
  VR Little Endian — bir hasta CD'sindeki MR dosyalarının büyük bölümü). Dosyaları
  sürükle-bırak ile de yükleyebilirsin.
- **Anında çalışan örnek beyin MR serisi** (22 kesit) — hiç dosyan olmadan öğrenmeye
  başlayabilirsin.
- **iQ-VIEW tarzı araçlar:**
  - Pencere / Seviye (kontrast & parlaklık) + hazır ayarlar (Beyin / Yumuşak Doku / Tam)
  - Kesitler arasında gezinme (fare tekerleği · ok tuşları · küçük resim şeridi)
  - Yakınlaştır / Kaydır
  - Milimetre cinsinden mesafe ölçümü (DICOM piksel aralığından)
  - Negatif (invert), ekrana sığdır, sıfırla
  - DICOM etiketleri paneli (hasta, modalite, sekans, TR/TE, kesit kalınlığı…)
- **8 bölümlük Türkçe öğretici:** DICOM temelleri, pencereleme, ölçüm, MR
  sekanslarını (T1/T2/FLAIR/DWI) tanıma ve sistematik okuma alışkanlığı.

## Kullanım

Kurulum yok. İki yol:

1. **En kolay:** `index.html` dosyasını çift tıkla — tarayıcıda açılır.
2. **GitHub Pages ile yayınla:** Depo ayarları → **Pages** → Branch: `main`, klasör: `/root`.
   Birkaç dakika içinde `https://<kullanıcı-adı>.github.io/mr-okuma-atolyesi/`
   adresinden herkes erişebilir.

## Kısayollar

| Tuş | İşlev |
|-----|-------|
| Fare tekerleği | Kesit değiştir |
| Ctrl + tekerlek | Yakınlaştır |
| ↑ ↓ ← → | Kesit değiştir |
| + / − | Yakınlaştır / uzaklaştır |
| `i` | Negatif (invert) |
| `r` | Sıfırla |

## Teknik notlar

- Saf HTML + CSS + JavaScript. Bağımlılık yok, derleme (build) yok.
- DICOM ayrıştırma tamamen tarayıcıda, kendi yazılmış hafif bir okuyucu ile yapılır.
- **Sıkıştırılmış** transfer sözdizimleri (JPEG / JPEG2000 / RLE) bu hafif okuyucuda
  desteklenmez; böyle dosyalar atlanır ve uyarı gösterilir.

## Lisans

MIT
