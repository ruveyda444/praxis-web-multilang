# Yüksel Arslan — Web Sitesi

Üç dilli (TR / EN / DE) psikolog tanıtım sitesi.

## Klasördeki dosyalar

| Dosya | Ne işe yarar |
|-------|--------------|
| `index.html` | **Statik sürüm.** Çift tıklayınca tarayıcıda açılır. GitHub Pages'te ücretsiz yayınlanır. Formu, ziyaretçinin e-posta uygulamasını açar. |
| `index.php` | **Backend dahil sürüm.** Form, e-postayı sunucudan gönderir. Yalnızca PHP destekli hosting'de çalışır. |
| `.gitignore` | Gereksiz dosyaların (ör. `.DS_Store`) GitHub'a gitmesini engeller. |

> İki sürüm de aynı görünür. Fark sadece iletişim formunun nasıl çalıştığıdır.

---

## 1. Bilgisayarda görmek
`index.html` dosyasına çift tıkla — tarayıcıda açılır. Kurulum gerekmez.

## 2. VS Code'da açmak
VS Code'u aç → **File > Open Folder** → bu klasörü (`praxis-web-multilang`) seç.
Canlı önizleme istersen "Live Server" eklentisini kurup `index.html` üzerinde "Go Live" diyebilirsin.

## 3. GitHub'a atmak (VS Code ile, en kolay yol)
1. VS Code'da sol taraftaki **Source Control** (dallanma) simgesine tıkla.
2. **Initialize Repository** de.
3. Değişiklikleri yazıp (commit message) **Commit** et.
4. **Publish to GitHub** butonuna bas, repo adını seç.

Komut satırını tercih edersen:
```
cd praxis-web-multilang
git init
git add .
git commit -m "İlk sürüm"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADIN/REPO_ADI.git
git push -u origin main
```

## 4. Yayınlama (deploy)
- **GitHub Pages (ücretsiz, statik):** Repo > Settings > Pages > Branch: `main` seç. Site `index.html`'i kullanır. **PHP burada çalışmaz** — form, e-posta uygulamasını açar.
- **PHP'li hosting (IONOS, Strato, all-inkl, cPanel...):** `index.php`'yi yükle, form sunucudan e-posta gönderir. Not: Aynı klasörde hem `index.html` hem `index.php` varsa, sunucu genelde `index.html`'i önceliklendirir — PHP'nin çalışması için `index.html`'i sil ya da yeniden adlandır.

---

## Yayından önce doldurulması gerekenler
- **Impressum** ve **Datenschutzerklärung** (footer'da, Almanya'da zorunlu) — `[...]` yer tutucuları gerçek bilgiyle doldur, hukuki kontrol yaptır.
- **Telefon** (şu an placeholder).
- **Ünvan** ("Psychotherapeut" Almanya'da korumalı ünvandır — gerçek statü doğru yazılmalı).
- **Randevu + DSGVO uyumlu video aracı** "Ücretsiz ön görüşme" butonuna bağlanmalı.
- `index.php` içindeki alıcı e-posta zaten ayarlı: `yukselarslan1071@gmail.com`.

Gizlilik durumu: site hiç çerez/izleyici kullanmaz, fontlar gömülüdür (Google'a bağlanmaz) → çerez banner'ı gerekmez.
