# 🌈 RGB'den CMYK'ya: Teknik Dönüşüm Rehberi

Dijital ortamda (AI çıktıları) kusursuz duran bir rengin fiziksel dünyada (baskı) aynı etkiyi yaratması için teknik denetim şarttır.

## Renk Uzayı Farkları
- **RGB (Red, Green, Blue):** Işık tabanlı, katkısal (additive) model. Gamut geniştir.
- **CMYK (Cyan, Magenta, Yellow, Key/Black):** Mürekkep tabanlı, eksiltici (subtractive) model. Gamut daha dardır.

## Teknik Parametreler
### 1. TAC (Total Area Coverage)
Baskıda kağıdın üzerine düşecek toplam mürekkep yoğunluğu limitidir.
- **Gazete Kağıdı:** ~%240
- **Kuşe Kağıt (Coated):** ~%300-%330
*AI çıktılarındaki derin siyahlar bu limiti genellikle aşar ve matbaada kağıdın kurumamasına veya yapışmasına neden olur.*

### 2. Delta E (ΔE) Standardı
Renk sapmasını ölçmek için kullanılan formül.
- **ΔE < 2.0:** İnsan gözü farkı ayırt edemez (Profesyonel Hedef).
- **ΔE 3.0 - 5.0:** Kabul edilebilir fark.

## AI Görüntülerini Baskıya Hazırlama
1. **Adobe Bridge/Photoshop:** ICC profili atayın (örn: Coated FOGRA39).
2. **Out-of-Gamut Warning:** Gamut dışı kalan 'elektrik mavi' veya 'fosforlu yeşil' gibi renkleri manuel olarak düzenleyin.
3. **Rich Black Kontrolü:** Siyahların sadece `K:100` değil, `C:40 M:30 Y:30 K:100` (veya destekleyici renklerle) derinleştirildiğinden emin olun.
