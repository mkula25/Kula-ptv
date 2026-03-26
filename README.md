# 📺 KULA IPTV PRO

<p align="center">
  <img src="https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet"/>
  <img src="https://img.shields.io/badge/WPF-Windows-0078D4?style=for-the-badge&logo=windows"/>
  <img src="https://img.shields.io/badge/LibVLC-3.0.20-FF6600?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Lisans-Kişisel_Kullanım-green?style=for-the-badge"/>
</p>

<p align="center">
  <b>Windows için gelişmiş, modern arayüzlü IPTV oynatıcı.</b><br/>
  M3U · Xtream Codes · MAC Portal · EPG · Altyazı · Kayıt ve daha fazlası.
</p>

---

## 🖥️ Ekran Görüntüsü

> *(Ekran görüntüsü eklenecek)*

---

## ✨ Özellikler

### 📋 Playlist Desteği
- **M3U / M3U8** URL veya yerel dosyadan kanal yükleme
- **Xtream Codes API** — sunucu, kullanıcı adı, şifre ile bağlantı
- **MAC Portal (Stalker)** — MAC adresi ile portal bağlantısı
- **Direkt Link** — HTTP/HTTPS stream ve YouTube URL desteği (yt-dlp ile)
- Birden fazla kayıtlı hesap yönetimi
- Playlist kaydetme ve geçmişten hızlı yükleme

### 📡 EPG (Elektronik Program Rehberi)
- **XMLTV** formatında EPG yükleme (URL veya dosya)
- M3U içindeki `url-tvg` / `tvg-url` başlığından **otomatik EPG yükleme**
- Xtream Codes bağlantısında **otomatik EPG yükleme** (`xmltv.php`)
- EPG verisi 6 saatten eskiyse otomatik yenileme
- Kanal listesinde anlık program adı ve ilerleme çubuğu
- **Tam EPG Rehber** penceresi — tüm kanalların programlarını gösteren grid

### 🎬 Video Oynatıcı (LibVLC)
- **Canlı TV**, **Film (VOD)** ve **Dizi** içerik tipi desteği
- Liste görünümü ve **Poster/Grid** görünümü
- Oynat / Duraklat / Durdur / Önceki / Sonraki kanal
- **15 saniye geri / ileri** sarma
- Ses seviyesi ayarı ve sessiz modu
- **Oynatma hızı** kontrolü (0.25× adımlarla, `+` / `-` / `0`)
- **Görüntü oranı** döngüsü (16:9 / 4:3 / Fill vb.)
- **Tam ekran** modu (çift tıklama veya `F` tuşu)
- **Mini Oynatıcı (PiP)** — pencere küçültülürken oynatmaya devam
- Kalite, ses izi ve altyazı izi seçimi (ComboBox)
- VLC **ağ önbellek** ayarı (kaydırıcı, 500–8000ms)
- **Otomatik yeniden bağlanma** (stream kesilince)

### 🎵 Ses ve Altyazı
- Ses izi seçimi (çoklu dil desteği)
- Altyazı izi seçimi
- **Harici altyazı** yükleme (`.srt` / `.ass` / `.vtt`)
- **OpenSubtitles** entegrasyonu:
  - Subdl.com ve OpenSubtitles.com API desteği
  - Uygulama içi API key yönetimi
  - Dil seçimi ile altyazı arama ve otomatik indirme

### ⭐ Favoriler ve Geçmiş
- Kanallara favori ekleme / çıkarma (yıldız butonu)
- Favori filtreleme modu
- **İzleme geçmişi** — son izlenen kanallar
- Favorileri M3U olarak dışa aktarma
- Tüm listeyi M3U olarak kaydetme

### 🔍 Arama ve Kategoriler
- Kanal / program adı arama (debounce ile)
- **Arama geçmişi** popup'ı
- Kategori sidebar'ı — gruba göre filtreleme
- **Grup özelleştirme** — kategori adı değiştirme, gizleme, sıralama

### 📡 Kanal Durum Kontrolü
- Seçili kanalların çevrimiçi/çevrimdışı durumunu toplu kontrol
- Kanal listesinde renk göstergesi (yeşil / kırmızı)

### ⏱️ Uyku Zamanlayıcısı
- Belirli süre sonra:
  - Yalnızca oynatmayı durdur
  - Uyku moduna geç
  - Hazırda beklet
  - Bilgisayarı kapat
  - Yeniden başlat
- Video üzerinde geri sayım göstergesi

### 🔒 Ebeveyn Kontrolü
- PIN ile kategori kilitleme
- PIN değiştirme ve kaldırma
- Kilitli kategoriye erişimde PIN sorma

### ⏺️ Kayıt
- Aktif kanalı kayıt altına alma (VLC sout)
- Kayıt süresi göstergesi
- Kayıt sırasında uygulama kapatılmaya çalışılırsa uyarı

### 📸 Ekran Görüntüsü
- Oynatma sırasında anlık ekran görüntüsü alma
- Masaüstüne kaydetme

### 🌐 Dil Desteği
- **Türkçe** ve **İngilizce** dil desteği
- Uygulama çalışırken tek tıkla dil değiştirme (`🌐 EN` / `🌐 TR`)
- Seçilen dil kaydedilir, bir sonraki açılışta hatırlanır

### 🔄 Otomatik Güncelleme
- GitHub Releases üzerinden güncelleme kontrolü
- Yeni sürüm varsa indirme sayfasına yönlendirme

### ⚡ Performans
- `VirtualizingPanel` ile büyük kanallı listelerde akıcı kaydırma
- `GuessKind` sonucu cache'leme — binlerce kanallı listelerde hızlı filtreleme
- Timer optimizasyonları (gereksiz UI güncellemeleri engellendi)
- Static `HttpClient` — soket tüketimi minimize edildi
- Toplu EPG güncelleme — N yerine tek `Dispatcher` çağrısı

---

## 🛠️ Gereksinimler

| Gereksinim | Versiyon |
|---|---|
| İşletim Sistemi | Windows 10 / 11 (64-bit) |
| .NET Runtime | .NET 8.0 |
| LibVLC | 3.0.20 (NuGet ile otomatik gelir) |

---

## 📦 Kurulum

### Hazır sürüm (önerilen)
1. [Releases](../../releases) sayfasından son sürümü indirin
2. ZIP'i çıkartın
3. `KULA.IPTV.PRO.exe` dosyasını çalıştırın

### Kaynak koddan derleme
```bash
git clone https://github.com/mustafakula/kula-iptv.git
cd kula-iptv
dotnet build -c Release
dotnet run
```

---

## 🚀 Kullanım

### İlk Kurulum
1. Uygulamayı açın
2. **🔌 Kaynaklar** sekmesine gidin
3. Aşağıdakilerden birini seçin:
   - **M3U · EPG** → M3U URL'nizi yapıştırın → *URL Yükle*
   - **Xtream Codes** → Sunucu, kullanıcı adı, şifre girin → *Bağlan ve Yükle*
   - **MAC Portal** → Portal URL ve MAC adresi girin → *MAC ile Bağlan*
   - **Link Ekle** → Direkt stream veya YouTube linki

### Klavye Kısayolları

| Tuş | İşlev |
|---|---|
| `Space` | Oynat / Duraklat |
| `F` veya `Enter` | Tam Ekran |
| `Esc` | Tam Ekrandan Çık |
| `M` | Sessiz |
| `↑` / `↓` | Ses ±5 |
| `←` / `→` | 10 sn Geri / İleri |
| `Ctrl+←` / `Ctrl+→` | Önceki / Sonraki Kanal |
| `+` / `-` | Hız Artır / Azalt |
| `0` | Hızı Sıfırla (1×) |
| `S` | Ekran Görüntüsü |
| `A` | Görüntü Oranı Değiştir |
| `P` | Mini Oynatıcı (PiP) |
| `Ctrl+R` | Kayıt Başlat / Durdur |
| `Ctrl+S` | Uyku Zamanlayıcısı |
| `F1` / `?` | Klavye Kısayolları |
| `Scroll` | Ses (video üzerinde) |
| Çift Tıklama | Tam Ekran Geçiş |

---

## 📁 Veri Dizini

Uygulama verileri şu dizinde saklanır:
```
%AppData%\KulaIPTV\
├── state.json          ← Ayarlar ve playlist geçmişi
├── subtitles\          ← İndirilen altyazılar
└── logs\               ← Uygulama logları
```

---

## 🔑 Altyazı API Anahtarları (Opsiyonel)

Altyazı araması için en az bir ücretsiz API key gereklidir:

| Servis | Kayıt Linki | Ücretsiz Limit |
|---|---|---|
| **Subdl.com** | [subdl.com/setting](https://subdl.com/setting) | 100 istek/gün |
| **OpenSubtitles** | [opensubtitles.com/api](https://www.opensubtitles.com/api) | 20 indirme/gün |

API key'leri uygulama içindeki altyazı arama penceresinden girebilirsiniz. Kaydedilir, tekrar sorulmaz.

---

## 🏗️ Teknolojiler

| Teknoloji | Kullanım Amacı |
|---|---|
| **.NET 8 / WPF** | Ana uygulama çatısı |
| **LibVLCSharp** | Video oynatma motoru |
| **LibVLC 3.0.20** | Media codec katmanı |
| **yt-dlp** | YouTube URL çözümleme |
| **System.Text.Json** | JSON serileştirme |
| **XMLTV** | EPG veri formatı |

---

## 📄 Lisans

Bu proje **kişisel kullanım** amacıyla geliştirilmiştir.  
Ticari kullanım ve yeniden dağıtım için izin gereklidir.

---

## 👤 Geliştirici

**Mustafa Kula**  
📧 [mustafakula25@gmail.com](mailto:mustafakula25@gmail.com)  
🐙 [github.com/mustafakula](https://github.com/mustafakula)

---

## ⭐ Destek

Uygulamayı beğendiyseniz GitHub'da **⭐ Star** vermeyi unutmayın!  
Hata bildirimi ve öneriler için [Issues](../../issues) bölümünü kullanabilirsiniz.

---

<p align="center">
  <i>KULA IPTV PRO — Güçlü, hızlı ve modern IPTV deneyimi.</i>
</p>
