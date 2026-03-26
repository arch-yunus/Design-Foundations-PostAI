# 🎮 ControlNet Derinlemesine Bakış (AI Kompozisyon Denetimi)

Geleneksel tasarımcının AI üzerindeki en güçlü hakimiyet aracı ControlNet teknolojisidir. Sadece prompt yazmak yerine, görselin iskeletini yönetmenizi sağlar.

## Temel Modeller ve Teknik Kullanım

### 1. Canny (Kenar Algılama)
Görselin konturlarını baz alır. Var olan bir çizimin veya eskizin kompozisyonunu değiştirmeden renklendirmek ve detaylandırmak için kullanılır.

### 2. Depth (Derinlik Haritası)
Görseldeki objelerin birbirine olan uzaklığını (Z-axis) analiz eder. Işıklandırma ve derinlik efektlerini (bokeh) korurken içeriği değiştirmek için idealdir.

### 3. OpenPose (Poz Kontrolü)
Karakterlerin duruşunu, el ve yüz hareketlerini eklemler üzerinden kilitler. İnsan figürü olan tasarımlarda anatomik hataları (AI'nın ünlü '6 parmak' sorunu gibi) minimize eder.

### 4. IP-Adapter (Style Transfer)
Bir referans görselin tarzını (renk paleti, ışık, stil) yeni bir kompozisyona aktarır. Kurumsal kimlik (brand identity) korumak için en kritik araçtır.

## Profesyonel İpucu
- **Weight Control:** ControlNet etkisini `0.4` ile `1.0` arasında ayarlayarak AI'nın yaratıcılığı ile sizin teknik sınırlarınız arasındaki dengeyi kurun.
- **Multi-ControlNet:** Aynı anda hem `Canny` hem `Depth` kullanarak tam kompozit kontrol sağlayın.
