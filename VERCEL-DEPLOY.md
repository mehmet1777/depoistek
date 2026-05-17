# 🚀 Vercel'e Deploy Rehberi

## 📋 Özet

Web formu **Vercel'de** (sabit URL) → Çalışanlar buraya girer
API sunucusu **PC'nde** (değişken URL) → Sistem her başlatmada yeni URL verir

---

## 🎯 Nasıl Çalışır?

### 1️⃣ İlk Kurulum (Bir Kere)

#### Vercel Hesabı Oluştur:
1. https://vercel.com/signup adresine git
2. GitHub ile giriş yap (ücretsiz)

#### Vercel CLI Yükle:
```bash
npm install -g vercel
```

#### Deploy Et:
```bash
cd "C:\Users\worda\Desktop\MGT Filtre\web-form"
vercel
```

Soruları yanıtla:
- **Set up and deploy?** → Y
- **Which scope?** → (hesabını seç)
- **Link to existing project?** → N
- **Project name?** → mgt-filtre
- **Directory?** → ./

✅ Deploy tamamlandı! URL'i kopyala: `https://mgt-filtre.vercel.app`

---

## 📱 Günlük Kullanım

### Her Sabah (PC'ni Açtığında):

#### 1. Sistemi Başlat:
```
MGT-Filtre-Baslat.vbs
```

#### 2. Cloudflare URL'ini Kopyala:
Launcher'dan URL'i kopyala:
```
https://xxxx-xxxx-xxxx.trycloudflare.com
```

#### 3. URL'i Paylaş:
WhatsApp grubuna mesaj at:

```
🔗 Bugünkü Sipariş Formu Bağlantısı:
https://xxxx-xxxx-xxxx.trycloudflare.com

📋 Form Linki (Sabit):
https://mgt-filtre.vercel.app

İlk girişte yukarıdaki bağlantı URL'ini yapıştırın!
```

---

## 👥 Çalışanlar İçin Talimat

### İlk Kullanım:

1. **Formu Aç:**
   ```
   https://mgt-filtre.vercel.app
   ```

2. **Popup Çıkacak:**
   ```
   🔗 MGT Filtre API URL'ini girin:
   (Sistem yöneticisinden alın veya WhatsApp grubunda 
   paylaşılan URL'i kullanın)
   ```

3. **WhatsApp'tan Kopyala:**
   Grup mesajındaki URL'i kopyala ve yapıştır:
   ```
   https://xxxx-xxxx-xxxx.trycloudflare.com
   ```

4. **Tamam'a Tıkla**
   Form açılır, sipariş verebilirsin!

### Sonraki Kullanımlar:

- Form URL'i hatırlar
- Direkt sipariş verebilirsin
- **Sadece** "Bağlantı hatası" alırsan → "🔄 API Bağlantısını Güncelle" butonuna tıkla

---

## 🔄 URL Değiştiğinde

### Senaryo:
PC yeniden başlatıldı → Cloudflare URL değişti

### Çözüm:

#### Yöntem 1: Çalışanlar Kendisi Günceller (Önerilen)
1. WhatsApp'a yeni URL'i at
2. Çalışanlar formda "🔄 API Bağlantısını Güncelle" butonuna tıklar
3. Yeni URL'i yapıştırır
4. Devam eder

#### Yöntem 2: Sen Güncelle (Eski Yöntem)
1. `index.html` dosyasını aç
2. Satır 23'teki URL'i değiştir
3. Vercel'e tekrar deploy et:
   ```bash
   vercel --prod
   ```

---

## 💡 İpuçları

### URL'i Sabitleştirmek İstersen:

**Ngrok Pro ($8/ay):**
- Sabit URL: `https://mgt-filtre.ngrok.io`
- Bir kere ayarla, sonsuza kadar kullan
- Web formunu hiç güncelleme

**Kurulum:**
```bash
ngrok config add-authtoken YOUR_TOKEN
ngrok http 8000 --domain=mgt-filtre.ngrok.io
```

### WhatsApp Mesajını Sabitle:

Grupta mesajı sabitle ki herkes kolayca bulsun:
```
📦 MGT Filtre Sipariş Formu

🌐 Form: https://mgt-filtre.vercel.app

🔗 Bugünkü Bağlantı:
https://xxxx.trycloudflare.com

(Her gün güncellenecektir)
```

---

## 🐛 Sorun Giderme

### "Stok listesi yüklenemedi"
- PC'de sistem çalışıyor mu?
- Cloudflare URL güncel mi?
- "🔄 API Bağlantısını Güncelle" butonuna tıkla

### "CORS hatası"
- `api.py` dosyasında CORS ayarları var
- Sorun devam ederse PC'yi yeniden başlat

### "Bağlantı zaman aşımı"
- İnternet bağlantını kontrol et
- PC'de firewall API'yi engelliyor olabilir

---

## 📊 Maliyet

| Servis | Fiyat | Özellik |
|--------|-------|---------|
| **Vercel** | Ücretsiz | Web form hosting (sabit URL) |
| **Cloudflare** | Ücretsiz | Tunnel (değişken URL) |
| **Ngrok Free** | Ücretsiz | Tunnel (bazen değişen URL) |
| **Ngrok Pro** | $8/ay | Tunnel (sabit URL) |

**Şu anki sistem:** Tamamen ücretsiz! ✅

---

## ✅ Tamamlandı!

Artık:
- ✅ Web formu Vercel'de (sabit URL)
- ✅ Çalışanlar WhatsApp'tan linke tıklayıp sipariş verebilir
- ✅ İlk girişte API URL'ini yapıştırırlar
- ✅ Sonraki kullanımlarda otomatik bağlanır
- ✅ URL değişirse "Güncelle" butonuna tıklarlar

🎉 Sistem hazır!
