# 📐 Vektörizasyon İş Akışları (Advanced Tracing)

AI tarafından üretilen raster (piksel) tabanlı görsellerin, profesyonel baskı ve ölçeklenebilirlik için vektöre çevrilme sürecidir.

## Raster vs Vector: Teknik Sınır
AI çıktıları (Midjourney/DALL-E) genellikle 72-96 DPI çözünürlüktedir. Bu görüntüler doğrudan baskıya verilirse "pixelation" kaçınılmazdır.

## İş Akışı (Workflow)
### Adım 1: Hazırlık (Luma/Contrast)
AI çıktısını Photoshop'ta açın, `Threshold` veya `Levels` kullanarak siyah-beyaz zıtlığını maksimize edin. Bu, vektörizasyon motorunun (trace engine) kenarları daha net görmesini sağlar.

### Adım 2: Teknik Tracing (Illustrator)
- **Mode:** Black and White or Color (limit colors).
- **Paths:** %90+ (Detay sadakati).
- **Corners:** %50 (Gürültüyü azaltmak için).
- **Noise:** 2px (Küçük piksel hatalarını görmezden gel).

### Adım 3: Bezier Eğrileri ve Anchor Points
Vektöre çevrilen görselde 'Anchor Point' sayısını minimize edin. Gereksiz noktalar görselin "titrek" (jittery) görünmesine neden olur. `Object > Path > Simplify` komutunu kullanarak matematiksel eğrileri pürüzsüzleştirin.

## Ne Zaman Vektör?
- Logo ve İkonlar: **ZORUNLU**
- Tipografik Tasarımlar: **ZORUNLU**
- Karmaşık İllüstrasyonlar: **HİBRİT** (Arka plan raster, ön plan vektör)
