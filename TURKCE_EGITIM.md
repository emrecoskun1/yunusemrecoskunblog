# 🎓 Unicorn Sparkle Portfolyo - Türkçe Eğitim Rehberi

## 📝 İçindekiler
1. [Proje Yapısı](#proje-yapısı)
2. [Türkçe Dil Desteği Ekleme](#türkçe-dil-desteği-ekleme)
3. [Kendi Bilgilerinle Güncelleme](#kendi-bilgilerinle-güncelleme)
4. [Proje Görselleri Ekleme](#proje-görselleri-ekleme)
5. [Deployment (Yayınlama)](#deployment)

---

## 🗂️ Proje Yapısı

```
unicorn-sparkle/
├── src/
│   ├── locales/          # Dil dosyaları
│   │   ├── en/           # İngilizce
│   │   ├── es/           # İspanyolca
│   │   └── tr/           # Türkçe (YENİ!)
│   ├── images/           # Görseller
│   │   ├── projects/     # Proje görselleri
│   │   └── contributions/# Katkı görselleri
│   ├── pages/            # Sayfalar
│   └── components/       # Bileşenler
└── public/               # Statik dosyalar
```

---

## 🌍 ADIM 1: Türkçe Dil Desteği Ekleme

### 1.1 Dil Dosyası Oluşturuldu ✅
`src/locales/tr/common.json` dosyası oluşturuldu ve tüm metinler Türkçeye çevrildi.

### 1.2 Routing Yapılandırması

Şimdi Türkçe rotasını ekleyelim. `src/routes/index.astro` dosyasını güncelleyin:

```astro
---
// Türkçe için yönlendirme ekleyin
const preferredLang = Astro.request.headers.get('accept-language');

if (preferredLang?.includes('tr')) {
  return Astro.redirect('/tr');
}

return Astro.redirect('/en');
---
```

### 1.3 Türkçe Sayfa Oluşturma

Yeni bir Türkçe sayfa oluşturun: `src/pages/tr.astro`

```astro
---
import Layout from '../layouts/Layout.astro';
import Hero from '../pages/_home/Hero.astro';
import Experience from '../pages/_home/Experience.astro';
import Projects from '../pages/_home/Projects.astro';
import Contributions from '../pages/_home/Contributions.astro';
import About from '../pages/_home/About.astro';
import Contact from '../pages/_home/Contact.astro';

const lang = 'tr';
const t = await import(`../locales/${lang}/common.json`);
---

<Layout title={t.title} description={t.description} lang={lang}>
  <Hero {lang} />
  <Experience {lang} />
  <Projects {lang} />
  <Contributions {lang} />
  <About {lang} />
  <Contact {lang} />
</Layout>
```

---

## ✏️ ADIM 2: Kendi Bilgilerinle Güncelleme

### 2.1 Kişisel Bilgileri Değiştir

`src/locales/tr/common.json` dosyasını açın ve şu bölümleri güncelleyin:

#### Hero (Ana Başlık)
```json
"hero": {
  "job_availability": "İş için müsait!",
  "title": "Merhaba, Ben [ADINIZ]!",
  "job_title": "<strong>[UNVANINIZ]</strong> - [ŞEHİR/ÜLKE]",
  "description": "[TEKNOLOJİLERİNİZ VE UZMANLıK ALLARINIZ]",
  "cta": "Benimle İletişime Geç"
}
```

#### Hakkımda
```json
"about": {
  "title": "Hakkımda",
  "subtitle": "[KENDİNİZİ TANITIN]",
  "description": "[DETAYLI AÇıKLAMANıZ - deneyim, beceriler, hedefler]"
}
```

### 2.2 Deneyim Bilgilerini Güncelle

```json
"experience": {
  "title": "İş Deneyimi",
  "jobs": {
    "jobs_title": ["[ŞİRKET 1]", "[ŞİRKET 2]"],
    "jobs_description": [
      {
        "title": "[POZİSYON ADI]",
        "time": ["[BAŞLANGIÇ TARİHİ]", "[BİTİŞ TARİHİ]"],
        "description": "[NE YAPTIĞINIZI AÇIKLAYIN]",
        "list": ["[SORUMLULUK 1]", "[SORUMLULUK 2]"]
      }
    ]
  }
}
```

---

## 📦 ADIM 3: GitHub Projelerinizi Ekleme

### 3.1 Proje Bilgilerini Düzenle

`src/locales/tr/common.json` içinde `projects` bölümünü güncelleyin:

```json
"projects": [
  {
    "title": "Blogium",
    "description": "Medium alternatifi blog platformu",
    "image": "/src/images/projects/blogium.jpg",
    "techs": ["TypeScript", "React", "Node.js"],
    "code": "Kod",
    "preview": "Önizleme"
  },
  // Daha fazla proje ekleyin...
]
```

### 3.2 Proje Görselleri Ekleme

1. Proje ekran görüntülerini hazırlayın (önerilen boyut: 1200x630px)
2. Görselleri `src/images/projects/` klasörüne kopyalayın
3. Görselleri `.jpg` veya `.png` formatında kaydedin

**Örnek:**
```bash
src/images/projects/
├── blogium.jpg
├── blog.jpg
├── fintech.jpg
├── restaurant.jpg
└── mvc.jpg
```

### 3.3 GitHub Linklerini Ekleme

Her proje için GitHub repository linkini ekleyin. 

Önce `src/locales/tr/common.json` şemasını güncelleyin:

```json
{
  "title": "Blogium",
  "description": "...",
  "image": "/src/images/projects/blogium.jpg",
  "techs": ["TypeScript", "React"],
  "github": "https://github.com/emrecoskun1/blogium",
  "demo": "https://blogium-demo.vercel.app",
  "code": "Kod",
  "preview": "Önizleme"
}
```

---

## 🎨 ADIM 4: Görselleri Optimize Etme

### 4.1 Görsel Boyutları
- **Proje görselleri:** 1200x630px (16:9 oran)
- **Katkı görselleri:** 800x600px
- **Profil fotoğrafı:** 400x400px (kare)

### 4.2 Görsel Formatları
- Modern tarayıcılar için: `.webp` veya `.avif`
- Geri dönüş için: `.jpg`

### 4.3 Görsel Optimizasyon Araçları
- [TinyPNG](https://tinypng.com/) - Sıkıştırma
- [Squoosh](https://squoosh.app/) - Format dönüştürme
- [ImageOptim](https://imageoptim.com/) - Mac kullanıcıları için

---

## 🔧 ADIM 5: Sosyal Medya Linkleri

`src/components/Social.astro` dosyasını güncelleyin:

```astro
---
const socials = [
  {
    name: 'GitHub',
    url: 'https://github.com/emrecoskun1',
    icon: 'github'
  },
  {
    name: 'LinkedIn',
    url: 'https://www.linkedin.com/in/yunus-emre-coskun1/',
    icon: 'linkedin'
  },
  {
    name: 'Email',
    url: 'mailto:your.email@example.com',
    icon: 'mail'
  }
];
---
```

---

## 🚀 ADIM 6: Test ve Önizleme

### 6.1 Yerel Geliştirme Sunucusu

Terminal'de projenin klasörüne gidin ve çalıştırın:

```bash
cd /Users/yunusemrecoskun/Downloads/portfolios-dev-main/unicorn-sparkle

# Bağımlılıkları yükle
pnpm install

# Geliştirme sunucusunu başlat
pnpm dev
```

Tarayıcınızda açın: `http://localhost:4321/tr`

### 6.2 Kontrol Listesi

- [ ] Tüm metinler Türkçe mi?
- [ ] Kişisel bilgiler doğru mu?
- [ ] Proje görselleri yüklendi mi?
- [ ] GitHub linkleri çalışıyor mu?
- [ ] Sosyal medya linkleri doğru mu?
- [ ] Responsive tasarım düzgün mü? (mobil, tablet, desktop)

---

## 🌐 ADIM 7: Deployment (Yayınlama)

### 7.1 Vercel ile Yayınlama (ÖNERİLEN)

1. [Vercel](https://vercel.com/) hesabı oluşturun
2. GitHub repository'nizi bağlayın
3. Import butonuna tıklayın
4. Framework: `Astro` seçin
5. Deploy edin!

### 7.2 Netlify ile Yayınlama

1. [Netlify](https://www.netlify.com/) hesabı oluşturun
2. "New site from Git" tıklayın
3. Repository'nizi seçin
4. Build command: `pnpm build`
5. Publish directory: `dist`
6. Deploy!

### 7.3 GitHub Pages ile Yayınlama

```bash
# Build al
pnpm build

# GitHub Pages'e yükle
# (Önce repository settings'den GitHub Pages'i aktif edin)
```

---

## 📚 ADIM 8: Gelişmiş Özelleştirmeler

### 8.1 Renkler ve Tema

`src/styles/global.css` dosyasını düzenleyin:

```css
:root {
  --color-primary: #your-color;
  --color-secondary: #your-color;
  --color-accent: #your-color;
}
```

### 8.2 Fontlar

Google Fonts eklemek için `src/layouts/Layout.astro`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
```

### 8.3 SEO Meta Tags

`src/locales/tr/common.json` içinde:

```json
{
  "title": "Yunus Emre Coşkun - Fullstack Developer",
  "description": "Türkiye'den Fullstack Developer. .NET, Angular, Docker uzmanı.",
  "keywords": "fullstack developer, .NET, Angular, Docker, web geliştirme",
  "og_image": "/og-image.jpg"
}
```

---

## 🐛 Sık Karşılaşılan Sorunlar

### Görsel Yüklenmiyor
- Görselin yolunu kontrol edin: `/src/images/...`
- Dosya adında Türkçe karakter kullanmayın
- Büyük/küçük harf duyarlılığına dikkat edin

### Türkçe Karakterler Bozuk
- `common.json` dosyasının UTF-8 encoding'de olduğundan emin olun
- JSON syntax hatası olmadığını kontrol edin

### Sayfa Yüklenmedi
- Terminal'de hata mesajlarını okuyun
- `pnpm dev` tekrar çalıştırın
- Browser cache'i temizleyin

---

## 💡 İpuçları

1. **Git Kullanın:** Her değişiklikten sonra commit yapın
   ```bash
   git add .
   git commit -m "Türkçe dil desteği eklendi"
   ```

2. **Yedek Alın:** Orijinal dosyaları koruyun

3. **Test Edin:** Her büyük değişiklikten sonra siteyi test edin

4. **Dokümantasyon:** Yaptığınız değişiklikleri not alın

---

## 🎯 Hızlı Başlangıç Checklist

- [x] ✅ Türkçe dil dosyası oluşturuldu (`src/locales/tr/common.json`)
- [ ] Türkçe sayfa rotası eklendi (`src/pages/tr.astro`)
- [ ] Kişisel bilgiler güncellendi
- [ ] GitHub projeleri eklendi
- [ ] Proje görselleri yüklendi
- [ ] Sosyal medya linkleri eklendi
- [ ] Yerel sunucuda test edildi
- [ ] Production'a deploy edildi

---

## 📞 Yardıma mı İhtiyacınız Var?

- **GitHub Issues:** Proje repository'sinde issue açın
- **Dokümantasyon:** [Astro Docs](https://docs.astro.build)
- **Topluluk:** [Astro Discord](https://astro.build/chat)

---

## 🎉 Tebrikler!

Artık kendi Türkçe portfolyo siteniz var! 

### Sonraki Adımlar:
1. Blog yazıları ekleyin
2. İletişim formu entegre edin
3. Google Analytics ekleyin
4. SEO optimizasyonu yapın
5. Performance iyileştirmeleri

**İyi Kodlamalar! 🚀**
