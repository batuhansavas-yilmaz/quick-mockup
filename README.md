# Quick Mockup

Tarayıcıda çalışan, kurulum gerektirmeyen mockup stüdyosu. Ekran görüntünü 3 telefon, 1 tablet ve 1 masaüstü çerçevesine yerleştir; arka planı, yazıları ve çerçeve rengini özelleştir; PNG olarak indir.

![Quick Mockup](preview.png)

## Özellikler

- Galeride 3 telefon + 1 tablet + 1 masaüstü; hero şablonu tek telefonla başlar, telefon/tablet/monitör eklenip kaldırılabilir
- Telefon, tablet ve masaüstü için 3D görünüm: döndürülebilir modeller; 3D çıktılar karedir; normal çıktılar cihaz oranındadır (telefon 9:16, tablet 4:3, masaüstü 16:9). 3D kartları diğer cihazlarla yan yana kalır; telefonlarda hero 3D da vardır
- Sağdaki sabit ayar paneli ekrana göre değişir: galeride arka plan + çerçeve, hero'da ek olarak yazı renkleri ve yazı stili
- Resim yükleme: sürükle-bırak veya alttaki Resim Değiştir / Resim Yükle butonu (ekrana tıklayarak değil)
- Görsel düzenleme: döndür, yatay/dikey aynala, yakınlaştır/uzaklaştır, sürükleyerek taşı, sıfırla
- Cihaz konumu: galeride cihazı doğrudan sürükleyerek konumlandırma; kart/floor kenarlarına mıknatıslı hizalama; görsel panlamak için Alt+sürükleme; konum PNG'ye yansır
- Hero'da taşırken kenar/merkez mıknatıslı hizalama ve mavi kılavuz çizgileri
- Hero'da metin kutuları kenar/köşelerden boyutlandırılabilir; metin kutusu genişliğine göre satırlanır
- Hero'ya harici fotoğraf ekleme; eklenen fotoğraf taşınır, boyutlandırılır, çoğaltılır ve silinir
- Hero'da Ctrl/Cmd+sürükle kopyalama; Delete/Backspace ile seçileni silme; cihazlardan model fark etmeksizin en az bir tane kalır
- Hero görsel araç çubuğu kontrollerin altında; resim eklenince aktif olur
- Arka plan: hazır gradyanlar (açı tümüne uygulanır), düz renkler, kendi çok renkli gradyanın (2–5 renk, açı), hex kodu, kendi arka plan resmin
- Hero arka plan resmi: taşıma, döndürme, aynalama, yakınlaştırma
- Yazı: 7 hazır font + kendi fontunu yükle (TTF/OTF/WOFF/WOFF2), 6 efekt (gölge, sert gölge, 3D, neon, kontur), boyut ve renk ayarı; metinler tıkla-düzenle
- Telefon çerçevesi rengi (hazır renkler + hex); iç çerçeve otomatik uyum sağlar
- Cihaz boyutu: her cihazda boyut kontrolüyle bağımsız büyütme/küçültme; en-boy oranı korunur, PNG'ye yansır
- RTX tarzı keskin cam yansıması: Düz, Neon ve 3D stillerinde açılıp kapanabilir
- Zemin butonu: kapalıyken sade görünüm; aktifken gerçekçi cilalı cam/ayna zemini yumuşak bir geçişle eklenir
- Galeride yansıma hizası sabittir; hero'da her telefon kendi tabanına göre yansır. Boyut küçülünce yansıma hizası sabit kalır
- Galeride cihaz başına bağımsız indirme boyutu ve stil
- Telefon çıktıları: 720×1280–2160×3840 (normal 9:16, 3D kare)
- Tablet çıktıları: 1024×768, 1536×1152, 2048×1536 (normal 4:3, 3D kare)
- Masaüstü çıktıları: 1920×1080, 3840×2160, 5760×3240 (normal 16:9, 3D kare)
- Hero çıktıları: 1280×800, 1600×1000, 1024×500, 2560×1600, 3840×2400
- İndirme stili: Düz, Neon, Dergi, Dergi 2 (sağa yatık), 3D; Neon seçili arka plan renklerinden üretilir; stil canlı önizlenir
- Mobil uyumlu: tek sütun düzen, panel içerik altında, dokunmatik taşıma ve büyük butonlar

## Performans ve 3D

3D döndürme `requestAnimationFrame` ile birleştirilir; sürükleme sırasında düşük çözünürlük, bırakınca yüksek kalite kullanılır. Renk değişimlerinde 3D modeller gereksiz yere yeniden üretilmez; yansıma güncellemeleri geciktirilir. 3D modeller prosedürel stüdyo ortam haritası, metal/cam materyalleri ve cihaza özel detaylar kullanır: telefonlarda kamera modülleri, tablette büyük gövde, masaüstünde ince çerçeveli 16:9 monitör ve stand. Ekran dokuları 2048 px çözünürlükte üretilir; galeri ve hero 3D görselleri aynı kalitededir. Galeride görsel döndürme/aynalama/zoom araçları tüm stillerde cihaz eylemlerinin altında ayrı bir araç çubuğunda gösterilir; araç çubuğu yalnızca ekrana resim eklendiğinde aktif olur. Döndürme tutamacı 3D sahnenin sol üst köşesinde sabittir; zemin tutamacı yansıma hizasını taşır.

## Lisanslar

- 8-bit font olarak gömülü **Press Start 2P** (Google Fonts, SIL Open Font License). Lisans metni: [`fonts/OFL.txt`](fonts/OFL.txt).
- 3D için **Three.js** (MIT). Lisans metni: [`vendor/THREE-LICENSE.txt`](vendor/THREE-LICENSE.txt).

## Kullanım

1. `index.html` dosyasını tarayıcıda aç (çift tıkla).
2. Cihaza tıkla ya da resmi sürükle-bırak.
3. **Arka Plan** panelinden özelleştir.
4. **Mockup İndir** / **PNG İndir** ile kaydet.

Kurulum, bağımlılık veya ağ bağlantısı gerekmez. Tüm işlemler tarayıcıda çalışır; hiçbir veri dışarı gönderilmez.
