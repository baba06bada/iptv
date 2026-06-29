# BABABADA PLAYER

LG WebOS 2.2.3+ (SmartTV 6.0) tarayıcılar için IPTV oynatıcı. Xtream Codes API ile çalışır.

## Özellikler

- Canlı TV, Film (VOD) ve Dizi izleme
- Xtream Codes API desteği (playlist URL + kullanıcı adı + şifre)
- HLS.js ile akıcı canlı yayın (otomatik yeniden bağlanma, takılma algılama)
- EPG (Elektronik Program Rehberi)
- Kanal gizleme/gösterme (basılı tut)
- Favori kanallar
- Sanal kaydırma (5000+ kanalda bile akıcı)
- OSD kontrolleri (ses, hız, kalite, en-boy oranı)
- Kaldığın yerden devam et (VOD/Dizi)
- Tam ekran desteği
- Magic Remote (WebOS) ve klavye desteği

## TV'de Kullanım

### GitHub Pages (Önerilen)

1. Bu repoyu GitHub'a yükle (repo adı: `iptv`)
2. Repo ayarlarından **Settings → Pages → Source: Deploy from branch → Branch: `main` → `/ (root)`** seç
3. Birkaç dakika içinde yayına girer:

```
https://baba06bada.github.io/iptv/LGTV.html
```

### jsDelivr CDN (Yedek, hiç ayar gerekmez)

GitHub'a yükledikten hemen sonra çalışır:

```
https://cdn.jsdelivr.net/gh/baba06bada/iptv@main/LGTV.html
```

### Local Test (Bilgisayarda)

```bash
http-server -c-1 -p 8080
# Tarayıcıda: http://localhost:8080/LGTV.html
# TV'de: http://192.168.0.x:8080/LGTV.html (TV aynı ağda olmalı)
```

## Kurulum

1. IPTV sağlayıcından aldığın **Xtream Codes URL, kullanıcı adı ve şifre** ile playlist ekle
2. Dashboard'dan playlistine tıkla
3. Kanal/film/dizi listesinden izlemek istediğini seç

## Uyumlu Cihazlar

- LG WebOS 2.2.3 – SmartTV 6.0 (Chrome 34)
- WebOS 3.x+ (daha yeni modellerde de çalışır)
- Diğer TV tarayıcıları (Samsung Tizen, Sony Android TV) – test edilmedi

## Teknik

- Tek dosya (LGTV.html): HTML + CSS + JavaScript (ES5, Chrome 34 uyumlu)
- HLS.js ile m3u8 akış desteği
- localStorage ile ayar saklama
- Magic Remote (keyCode) ve air mouse desteği
