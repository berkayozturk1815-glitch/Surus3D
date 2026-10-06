# Serbest Sürüş 3D

Tarayıcıda oynanan 3D araba oyunu: serbest sürüş, zombi modu (dalgalar, geliştirmeler, özel zombi türleri) ve yarış modu (3 pist, yapay zekâ rakipler). Kurulum gerektirmez; bilgisayar, tablet ve telefonda çalışır. Telefonda ana ekrana eklenip uygulama gibi açılabilir.

## GitHub Pages'e yayınlama (git bilmen gerekmez)

1. https://github.com adresinde giriş yap, sağ üstte **+ → New repository** de.
2. Depo adını yaz (örnek: `surus3d`), **Public** seç, **Create repository** de.
3. Açılan sayfada **uploading an existing file** bağlantısına tıkla.
4. Bu klasörün **içindeki her şeyi** (index.html, manifest.json, sw.js, 404.html, favicon.ico, robots.txt, README.md, LICENSE-THREEJS.txt ve `icons` klasörü) sürükleyip bırak. `.nojekyll` dosyası görünmüyorsa sorun değil, zorunlu değil.
5. Aşağıda **Commit changes** de.
6. Depoda **Settings → Pages** bölümüne git. **Source** olarak **Deploy from a branch** seç, **Branch:** `main`, klasör `/ (root)` seç, **Save** de.
7. 1-2 dakika bekle. Aynı sayfada oyunun adresi çıkar:

   `https://KULLANICI-ADIN.github.io/surus3d/`

   Bu adresi paylaşan herkes oyunu doğrudan açıp oynayabilir. (HTTPS otomatik gelir.)

İstersen depoyu `KULLANICI-ADIN.github.io` adıyla oluştur; o zaman adres kısa olur: `https://KULLANICI-ADIN.github.io/`

### Git ile (isteyenler için)

```bash
git init
git add .
git commit -m "Serbest Surus 3D"
git branch -M main
git remote add origin https://github.com/KULLANICI-ADIN/surus3d.git
git push -u origin main
```

Sonra yukarıdaki 6. adımı uygula.

## Güncelleme

`index.html` dosyasını depoda yenisiyle değiştir (Add file → Upload files). Oyuncular sayfayı yenileyince yeni sürümü görür. Çevrimdışı önbellek sürümünü değiştirmek istersen `sw.js` içindeki `surus3d-v6` yazısındaki sayıyı artır.

## Ana ekrana ekleme

- **iPhone / iPad (Safari):** Paylaş düğmesi → **Ana Ekrana Ekle**
- **Android (Chrome):** menü (⋮) → **Uygulamayı yükle** veya **Ana ekrana ekle**
- **Bilgisayar (Chrome / Edge):** adres çubuğundaki **Yükle** simgesi

Telefonda oyun yatay (ekranı yan çevir) en rahat oynanır.

## Kontroller

| | Bilgisayar | Telefon |
|---|---|---|
| Gaz / fren | W S veya ↑ ↓ | ▲ ▼ düğmeleri |
| Direksiyon | A D veya ← → | ◀ ▶ düğmeleri |
| El freni (drift) | Boşluk | EL FRENİ |
| Turbo | Shift | 🔥 |
| Kamera | C | 📷 |
| Gece / gündüz | T | menüdeki düğme |
| Yağmur | Y | menüdeki düğme |
| Duraklat | P veya Esc | ⏸ |
| Ses aç/kapat | M | menüdeki düğme |
| Zombi modunda geliştirmeler | U | 🛠 Geliştir |
| Garaj (menü) | G | Garaj |

## Dosyalar

- `index.html`: Oyunun kendisi (tek dosya; three.js ve 3B modeller içinde gömülü)
- `manifest.json`, `sw.js`, `icons/`, `favicon.ico`: Ana ekrana ekleme ve çevrimdışı çalışma
- `404.html`: Yanlış adreslerde oyuna yönlendirir
- `LICENSE-THREEJS.txt`: Kullanılan three.js kütüphanesinin lisansı (MIT)

Oyun internet gerektiren başka bir hizmet kullanmaz; sunucu, hesap ya da veritabanı yoktur. Rekorlar yalnızca oyuncunun kendi tarayıcısında saklanır.
