# Salon — GitHub Pages kurulumu

Bu klasörde iki dosya var:

- **index.html** — uygulamanın kendisi
- **catalog.json** — yayınlanan film listesi (şimdilik boş: `[]`)

## 1) Repoyu kur (tek seferlik)

1. GitHub'da yeni bir repo aç (örn. `salon`). Public olabilir.
2. `index.html` ve `catalog.json` dosyalarını reponun **köküne** yükle.
3. Repo → **Settings → Pages** → "Build and deployment" altında Source: **Deploy from a branch**, Branch: **main** / **/(root)** seç, kaydet.
4. Birkaç dakika sonra adresin hazır olur: `https://izzetfiratorfa.github.io/salon/`

Bu adresi Nur'a ve ailene ver. İlk girişte parola **3312** istenir (Ayarlar'dan değiştirilebilir).

## 2) Film ekleme / güncelleme (her seferinde)

Filmleri her zaman **sen** ekley:

1. Siteyi aç, **Yönet (⚙) → Kayıt ekle** ile filmleri ekle/düzenle.
2. İşin bitince **Yönet → catalog.json** ile dosyayı indir.
3. İndirdiğin `catalog.json`'u repodaki eskisiyle **değiştir** (commit et).

Bu kadar. Bir sonraki açılışta **herkesin** cihazı yeni listeyi otomatik alır — daha önce girmiş olsalar bile.

## Nasıl çalışıyor?

- Uygulama açılışta repodaki `catalog.json`'u okur.
- Yayınlanan `catalog.json` **değiştiğinde** tüm cihazlar yeni veriyi alır.
- Senin henüz indirip commit'lemediğin yerel düzenlemelerin, sen yayınlayana kadar yalnızca senin cihazında durur (kaybolmaz).

## Önemli notlar

- Dosyayı **çift tıklayıp `file://` olarak açma** — tarayıcı güvenlik gereği `catalog.json`'u okumaz. Mutlaka GitHub Pages adresinden (https) aç.
- Parola ve TMDB anahtarı uygulamanın içinde/sahte değil, tarayıcıda saklanır; bu basit bir kilittir, gerçek gizlilik sağlamaz. Repo public ise TMDB anahtarın da görünür olur (TMDB anahtarları düşük riskli, salt-okunur).
- Poster/afiş alanına **doğrudan görsel linki** (`.jpg`/`.png`) gir; IMDb'den çekersen poster otomatik gelir.
