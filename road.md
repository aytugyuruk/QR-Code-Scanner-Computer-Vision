## Proje 5: Barkod / QR Kod Okuyucu (Sadece Tespit Kısmı)

### Gerçek Hayat Uygulaması
Mağaza otomasyonu, envanter takibi, bilet kontrolü, bilgi paylaşımı.

### Neden Senin İçin Uygun?
Görüntü gradyanları ve morfolojik operasyonlar gibi daha ileri seviye görüntü işleme tekniklerini kullanmanızı gerektirir. *Not: Kodun içini çözmek yerine sadece konumunu bulmaya odaklanacaksınız.*

### Kullanacağın Temel Teknikler
- Sobel operatörü (`cv2.Sobel`) ile x ve y yönlerindeki gradyanları (kenar yoğunluklarını) hesaplama
- Gradyanları birleştirerek barkod/QR kod benzeri yoğun bölgeleri bulma
- Bulanıklaştırma ve Eşikleme
- Morfolojik operasyonlar (`cv2.morphologyEx` ile 'closing') ile barkod alanındaki boşlukları kapatıp tek bir bütün olarak algılanmasını sağlama
- Bulunan bölgenin etrafına bir kutu çizme

**Zorluk Seviyesi:** İleri