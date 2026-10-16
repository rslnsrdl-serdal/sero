# 🌍 Dünya Atlası — GeoQuest

Türkçe, mobil uyumlu ve ücretsiz dünya coğrafyası öğrenme oyunu.

## 🎮 İçerik
- 🚩 **Bayrak Avcısı:** Bayraktan ülke bul.
- 🏛️ **Başkent Ustası:** Başkentleri öğren.
- 🗺️ **Harita Dedektifi:** Gerçek ülke siluetini tanı.
- 🗣️ **Diller Dünyası:** Resmî dilleri öğren.
- 👑 **Kim Yönetiyor?:** Devlet veya hükûmet başkanlarını tanı.
- 🧭 **Kıta Kâşifi:** Ülkelerin kıtasını bul.
- 💰 **Para Birimleri:** Kullanılan para birimlerini eşleştir.
- 🎲 **Dünya Maratonu:** Modları karıştır.
- 🌐 **Ülke Atlası:** Ülkeler, bayraklar, başkentler, diller, sınırlar ve daha fazlası.
- 🎯 **Tekrar çalış:** Yanlış soruları cihazında sakla.
- ⭐ **XP, seri ve sayaç:** Her soru 20 saniye. Puan bonusu kalan süreye bağlı.

## 🌐 Oyna

GitHub Pages açıldıktan sonra uygulama adresi:

**https://rslnsrdl-serdal.github.io/sero/**

### GitHub Pages ilk kurulum (depo sahibi için)
1. [Bu deponun Pages ayarlarına](https://github.com/rslnsrdl-serdal/sero/settings/pages) gir.
2. **Build and deployment → Source → Deploy from a branch** seç.
3. **Branch: main** ve **Folder: /(root)** seçip **Save** düğmesine bas.
4. GitHub Pages yayınlamayı bitirince yukarıdaki bağlantıdan oyunu aç.

Yalnızca statik HTML/CSS/JavaScript kullanır; build komutu veya API anahtarı gerektirmez. Dış ülke ve harita verilerinin yüklenmesi için internet bağlantısı gerekir.

## 📊 Kapsam ve veri doğruluğu

- **Ülkeler:** [mledoze/countries](https://github.com/mledoze/countries), yaklaşık 250 ülke ve bölge kaydı. Bağımsız ülkeler ile bağlı bölgeler ayrı kapsam seçenekleri olarak sunulur. Kaynağa yeni kayıt eklenmesi halinde uygulama da onu görüntüleyebilir.
- **Bayraklar:** [FlagCDN](https://flagcdn.com/) ve Unicode bayrak emojisi.
- **Siluetler:** [world-atlas](https://github.com/topojson/world-atlas) ülkeler-50m, Natural Earth sınırlarından. Bazı çok küçük veya tartışmalı bölgeler için siluet bulunmayabilir.
- **Güncel yönetici soruları:** [open-data-archive/world-leaders-current](https://github.com/open-data-archive/world-leaders-current), güncel kayıt sağlanan yaklaşık **28 ülke**. Veri akışı ASEAN+G20 odaklıdır; tüm dünya liderlerinin eksiksiz veri tabanı değildir. Uygulama veri tarihini açıkça gösterir. Liderlik durumu hızlı değişebildiğinden kritik kullanım öncesi resmî kaynakla doğrula.

**Kapsam notu:** Bayrak, başkent, kıta, para ve dil oyunları ülke verisi olan kayıtlarda çalışır. Siluet ve yönetici modu yalnızca uygun veri bulunan kayıtlar için soru sorar. Ülke sınırları, tanınma statüsü ve başkent statüsü ihtilaflı olabilir.

## 🧪 Teknik
- Tek dosya: `index.html`
- Responsive, dokunmatik uyumlu, localStorage ilerleme kaydı
- Dış kütüphane veya sunucu kurulumu yok
- Açık kaynak kaynaklarına bağlantılar kodun ve uygulamanın altındadır


## 🎉 GeoQuest Live: PIN ile çok oyunculu yarışma

**[Canlı yarışmaya gir](https://rslnsrdl-serdal.github.io/sero/live.html)** (GitHub Pages etkinleştirildikten sonra)

1. Bilgisayar, tablet veya bir telefondan `live.html` sayfasını açıp **Yarışma oluştur** seç.
2. Soru türü (karışık, bayrak, başkent, siluet, diller, kıta, para birimi veya yönetici), kıta, soru sayısı (10/15/20/30) ve süre (10/20/30 saniye) belirle.
3. 6 haneli oyun PIN'ini veya katılım bağlantısını oyuncularla paylaş.
4. Oyuncular kendi telefonlarından **PIN ile katıl** seçip takma ad girer.
5. Oyuncular geldiğinde **Yarışmayı başlat**. Sorular aynı anda açılır, herkes cihazından işaretler.
6. Süre dolduğunda veya herkes cevapladığında doğru cevap ve canlı sıralama gösterilir. Sunucu sonraki soruyu açar.
7. Finalde podyum ve puan tablosu gösterilir; aynı odada yeniden başlatılabilir.

### Teknik ve güvenilirlik

- **PeerJS 1.5.5 + WebRTC** ile sunucu tarayıcısı ve oyuncu cihazları arasında doğrudan veri bağlantısı kurulur; bu ilk sürümde ayrı bir backend, hesap veya API anahtarı gerektirmez.
- Oyun PIN'i bağlantı kimliğine dönüştürülür; [PeerJS Cloud](https://peerjs.com/server/cloud) (üçüncü taraf ücretsiz sinyal sunucusu) kullanılır. Sunucunun tüm oyun boyunca açık ve internete bağlı kalması gerekir.
- **Üretim ölçeğinde garantili servis değildir.** Genel ağlar, kurumsal güvenlik duvarları, NAT, mobil tarayıcılar veya ücretsiz sinyal servisinin kesintileri bağlantıyı engelleyebilir. Geliştirme/test sürümü; özellikle küçük gruplar için uygun (öneri: 2–15 kişi; yazılımdaki üst sınır: 30).
- PIN yalnızca kolay katılım içindir, güçlü erişim kontrolü değildir. PIN'i bilen başka biri odaya girmeyi deneyebilir. Hassas bilgiler veya gerçek kimlik bilgileri kullanmayın; yalnızca takma ad girin.
- Puanlar sunucu cihazında hesaplanır; yarışma geçmişi sunucuda kalıcı olarak depolanmaz.
- Yönetici veri kaynağı tüm dünyayı kapsamaz ve siyasi görevler değişebilir. Bu bölümü resmî kaynaklarla yeniden teyit edin.

### Dosyalar

- `index.html`: Kişisel coğrafya oyunu + GeoQuest Live bağlantısı
- `live.html`: PIN ile çok oyunculu canlı yarışma (ayrı ekran)

## 💡 Geliştirme fikirleri
Haritada şehir seçme, zaman sınırı olmayan öğrenme modu, Türkçe–Almanca–İngilizce arayüz, iki kişilik yarışma, offline destek ve günlük görevler.
