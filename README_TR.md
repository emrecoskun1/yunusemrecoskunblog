# 🦄 Yunus Emre Coşkun - Kişisel Portfolyo

Bu proje, **Unicorn Sparkle** teması kullanılarak Türkçe olarak özelleştirilmiş kişisel portfolyo sitesidir.

## 🚀 Hızlı Başlangıç

```bash
# Projeyi klonlayın
cd unicorn-sparkle

# Bağımlılıkları yükleyin
pnpm install

# Geliştirme sunucusunu başlatın
pnpm dev
```

Tarayıcınızda açın: http://localhost:4321

## 📁 Proje Yapısı

```
unicorn-sparkle/
├── src/
│   ├── locales/
│   │   ├── tr/              # 🇹🇷 Türkçe çeviriler
│   │   ├── en/              # 🇬🇧 İngilizce çeviriler
│   │   └── es/              # 🇪🇸 İspanyolca çeviriler
│   ├── images/
│   │   ├── projects/        # Proje görselleri
│   │   └── contributions/   # Katkı görselleri
│   ├── pages/
│   ├── components/
│   └── layouts/
└── public/
```

## ✨ Özellikler

- ✅ Türkçe dil desteği
- ✅ Responsive tasarım
- ✅ Dark/Light mode
- ✅ SEO optimize
- ✅ Hızlı yükleme
- ✅ Modern UI/UX

## 🛠️ Teknolojiler

- **Framework:** Astro
- **Styling:** CSS
- **Icons:** Astro Icon
- **i18n:** Astrolicious i18n
- **Deployment:** Vercel / Netlify

## 📝 Özelleştirme

### 1. Kişisel Bilgilerinizi Değiştirin

`src/locales/tr/common.json` dosyasını açın ve bilgilerinizi güncelleyin:

- Adınız, ünvanınız
- İş deneyimleriniz
- Projeleriniz
- Hakkınızda bilgiler

### 2. Proje Görselleri Ekleyin

Proje görsellerinizi `src/images/projects/` klasörüne ekleyin ve `common.json` içinde referans verin.

### 3. Sosyal Medya Linkleri

`src/components/Social.astro` dosyasında sosyal medya linklerinizi güncelleyin.

### 4. Renkler ve Tema

`src/styles/global.css` dosyasında renk paletinizi özelleştirin.

## 🌍 Dil Değiştirme

Site varsayılan olarak Türkçe açılır. Navbar'daki dil seçici ile İngilizce ve İspanyolca arasında geçiş yapabilirsiniz.

## 📦 Build ve Deploy

### Build

```bash
pnpm build
```

### Önizleme

```bash
pnpm preview
```

### Deploy (Vercel)

1. GitHub'a push yapın
2. Vercel'e import edin
3. Deploy!

## 📚 Dokümantasyon

Detaylı Türkçe eğitim için `TURKCE_EGITIM.md` dosyasına bakın.

## 🔗 Linkler

- **Demo:** [yunusemrecoskun.xyz](https://yunusemrecoskun.xyz)
- **GitHub:** [github.com/emrecoskun1](https://github.com/emrecoskun1)
- **LinkedIn:** [linkedin.com/in/yunus-emre-coskun1](https://www.linkedin.com/in/yunus-emre-coskun1/)

## 📄 Lisans

Bu proje MIT lisansı altındadır.

## 🙏 Teşekkürler

- Orijinal tema: [Unicorn Sparkle](https://github.com/felixicaza/portfolios-dev)
- İkonlar: [Astro Icon](https://github.com/natemoo-re/astro-icon)

---

**Geliştirici:** Yunus Emre Coşkun  
**İletişim:** [GitHub](https://github.com/emrecoskun1)
