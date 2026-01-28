# 🚀 Yunus Emre Coşkun - Portfolyo

Modern ve responsive portfolyo sitesi. Astro ile geliştirilmiş, Türkçe dil desteği eklenmiş.

## 📝 Görselleri Nasıl Eklerim?

### 1. Profil Fotoğrafı
Profil fotoğrafını şu konuma kopyala:
```
src/images/yunusemrecoskun.jpg
```

Sonra `src/locales/tr/common.json` içinde profil fotoğrafı yolunu güncelle.

### 2. Proje Görselleri

Attığın görselleri şu klasöre kopyala:
```
src/images/projects/
├── blogium.jpg (Blogium projesi için)
├── medantalya.jpg (Med Antalya projesi için)  
└── neovakif.jpg (NeoVakıf projesi - attığın görseller)
```

**NeoVakıf Görselleri:** 
- Attığın ekran görüntülerinden birini seç
- `neovakif.jpg` olarak kaydet
- `src/images/projects/` klasörüne kopyala

## 🌐 Cloudflare Pages'e Deploy

### 1. Build Komutu:
```bash
pnpm build
```

### 2. Output Klasörü:
```
dist
```

### 3. Cloudflare Pages Ayarları:
- Framework preset: `Astro`
- Build command: `pnpm build`
- Build output directory: `dist`
- Node version: `18` veya üzeri

## 📦 Güncellediğim Dosyalar

✅ Türkçe dil dosyası oluşturuldu
✅ Kişisel bilgiler güncellendi
✅ Proje linkleri eklendi:
  - Blogium: https://blogium-w54e.onrender.com/
  - Med Antalya: https://medantalya.com/
✅ LinkedIn: https://www.linkedin.com/in/yunus-emre-coskun1/
✅ GitHub: https://github.com/emrecoskun1
✅ Footer güncellendi
✅ Gereksiz dosyalar silindi

## 🎨 Kişiselleştirme

`src/locales/tr/common.json` dosyasını düzenle:
- Hero section (Ana başlık)
- About (Hakkımda)
- Experience (Deneyim)
- Projects (Projeler)

## 🚀 Yerel Test

```bash
pnpm astro dev
```

Tarayıcıda aç: http://localhost:4321/

## 📸 Görselleri Ekleme Adımları

1. **Blogium görseli:** Blogium projesinin ekran görüntüsünü al, `blogium.jpg` olarak kaydet
2. **Med Antalya görseli:** Med Antalya sitesinin ekran görüntüsünü al, `medantalya.jpg` olarak kaydet  
3. **NeoVakıf görseli:** Attığın görselleri `neovakif.jpg` olarak kaydet
4. **Profil fotoğrafı:** Kendinin fotoğrafını `src/images/yunusemrecoskun.jpg` olarak kaydet

Tüm görseller `src/images/projects/` klasörüne gelecek!

## ✨ Tamamlandı!

Site hazır, Cloudflare Pages'e deploy edebilirsin! 🎉
