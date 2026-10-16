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

## 💡 Geliştirme fikirleri
Haritada şehir seçme, zaman sınırı olmayan öğrenme modu, Türkçe–Almanca–İngilizce arayüz, iki kişilik yarışma, offline destek ve günlük görevler.
