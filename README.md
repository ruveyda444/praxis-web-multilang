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

## 4. İletişim formu nasıl çalışır (önemli)
Form mesajı **yukselarslan1071@gmail.com**'a ulaşır. İki mod var:

1. **Doğrudan gönderim (önerilen, sunucu gerekmez):** `index.html` içinde
   `const FORM_ACCESS_KEY = '';` satırına ücretsiz bir Web3Forms anahtarı yapıştır:
   [web3forms.com](https://web3forms.com) → e-postanı gir → ücretsiz "Access Key" al → tırnakların arasına koy.
   Ziyaretçi formu doldurup gönderince e-posta doğrudan gider, "Teşekkürler" mesajı görünür.
   Sunucu/PHP gerekmez, anahtar dolmaz → **ömürlük, az bakım.**
2. **Anahtar boşsa (varsayılan):** Form, ziyaretçinin e-posta uygulamasını açar (mailto). Hiçbir şey kırılmaz, ama ekstra adım gerektirir.

> `index.php` (PHP sürümü) artık **gerekli değil.** Yukarıdaki Web3Forms yolu PHP'li hosting ihtiyacını ortadan kaldırır. İstersen PHP'li hosting kullanırsan diye dosya repoda duruyor.

## 5. Yayınlama (deploy)
- **GitHub Pages / Netlify / Cloudflare Pages (ücretsiz, statik):** sadece `index.html` yeterli. Web3Forms anahtarı eklenmişse form doğrudan çalışır.
- **PHP'li hosting (opsiyonel):** `index.php`'yi yükle. Aynı klasörde hem `index.html` hem `index.php` varsa sunucu genelde `index.html`'i önceliklendirir — PHP'yi kullanacaksan `index.html`'i sil/yeniden adlandır.

---

## Yayından önce doldurulması gerekenler (yalnızca senin verebileceğin bilgiler)
- **Telefon** — şu an placeholder (`+49 ...`).
- **Açık adres** — Impressum ve iletişim bölümü için (Heidelberg + sokak/no).
- **Ünvan / mesleki statü** — sitede "Psikolog · Psikoterapist" yazıyor. Almanya'da **"Psychotherapeut" korumalı ünvandır**; gerçek statünü (ör. *Heilpraktiker für Psychotherapie* izni var mı, yoksa "psychologische Beratung" mı) doğru yansıtmak gerekir. Uydurulamaz — bir uzmana danış.
- **Impressum + Datenschutzerklärung** — footer'da hazır şablon var; `[...]` alanlarını gerçek bilgiyle doldur, hukuki kontrol yaptır (Almanya'da yasal zorunlu).
- **Web3Forms anahtarı** — yukarıdaki forma yapıştırılacak (5 dk, ücretsiz).
- **Randevu + DSGVO-uyumlu video aracı** (ör. MeetOne/Jitsi) "Ücretsiz ön görüşme" butonuna bağlanacak.

Gizlilik durumu: site hiç çerez/izleyici kullanmaz, fontlar gömülüdür (Google'a bağlanmaz) → çerez banner'ı gerekmez.
