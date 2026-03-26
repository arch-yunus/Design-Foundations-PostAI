# 🖋️ Değişken Fontlar ve Optik Boyutlandırma (Variable Fonts)

Post-AI döneminde tipografi, statik bir seçimden ziyade dinamik bir mühendislik sürecidir.

## Variable Font Nedir?
Tek bir font dosyasının içinde birden fazla ağırlık (Weight), genişlik (Width) ve eğiklik (Slant) gibi eksenlerin (Axes) barındırılmasıdır.

### Temel Eksenler (Standard Axes)
1. **Weight (`wght`):** İnce (Hairline) ile Çok Kalın (Black) arasındaki geçiş.
2. **Width (`wdth`):** Dar (Condensed) ile Geniş (Expanded) arası.
3. **Slant (`slnt`):** Dik ile Eğik arası.
4. **Optical Size (`opsz`):** Fontun boyutuna göre form değiştirmesi.

## Optical Sizing (Optik Boyutlandırma) Neden Önemli?
AI tarafından üretilen tasarımlarda küçük puntolu metinlerde okunabilirlik sorunu yaşanır. `opsz` ekseni sayesinde:
- **6pt - 12pt:** Harf boşlukları artar, ince çizgiler (stems) kalınlaşır.
- **72pt+:** Detaylar keskinleşir, harf formları daha zarif hale gelir.

## Teknik Kontrol Listesi
- [ ] Fontun variable (değişken) olup olmadığını kontrol et.
- [ ] CSS'de `font-variation-settings` kullanarak eksenleri optimize et.
- [ ] AI görselindeki metin hiyerarşisini bu eksenlerle manuel olarak "re-balance" et.
