# EP 01 · Varlık Envanteri — Yangın Pompa Seti + S Plus Connect

Sunumdaki altı kategoriyle çıkarılmıştır; her kategoride üç kez "başka?" diye sorulmuştur. "Doğrulanacak" işaretli kalemler firmadan teyit edilmelidir.

**Sonuç:** "Pompa, pano, motor" diye başlayan liste, sistematik sayım sonrası **27 varlık + 6 dış bağlantıya** çıkıyor. Bunların 9'u emniyet yolunun parçası (D1–D9); servis dizüstüsü ve USB de pano ayarına erişirse bu yola dokunabiliyor. Ayrıca 7 hesap ve 6 kritik veri akışı var.

## 1 · Donanım

| # | Varlık | Zone | Emniyet yoluna dokunur mu? | Not |
| --- | --- | --- | --- | --- |
| D1 | Elektrikli ana pompa + motor | Z1 | Evet | |
| D2 | Dizel yedek pompa + motor | Z1 | Evet | |
| D3 | Jokey (kaçak tamamlama) pompası | Z1 | Evet | |
| D4 | Basınç anahtarları (en az 2, kilitli) | Z1 | Evet | Çalışma komutunu üreten eleman |
| D5 | Elektrik pompa kumanda panosu (Standart / Premium) | Z1 | Evet | İçinde PLC / elektronik kart var mı: doğrulanacak |
| D6 | Dizel pompa kumanda panosu + dizel kontrol ünitesi | Z1 | Evet | Start denemeleri, aşırı hız, akü |
| D7 | Jokey pompa panosu | Z1 | Evet | |
| D8 | Haftalık test zamanlayıcısı + selenoid vana | Z1 | Evet | |
| D9 | Akü 1 / Akü 2 ve şarj cihazı | Z1 | Evet | |
| D10 | Opsiyonel debimetre, vana izleme anahtarları | Z1 | Hayır (izleme) | Katalogda isteğe bağlı |
| D11 | S Plus Connect ağ geçidi kutusu | Z2 | Hayır (tasarım şartı) | Önerilen ürün |
| D12 | 4G modem / SIM kart | Z2 | Hayır | Telsiz ekipman → RED kapsamı |
| D13 | Bina otomasyon sistemi (BMS) kontrolcüsü | Z3 | Hayır (tasarım şartı) | Binaya ait |
| D14 | Yangın alarm paneli | Z3 | Hayır | Binaya ait |
| D15 | Servis teknisyeni dizüstüsü | Z5 | Pano ayarı yapılırsa evet | |
| D16 | USB bellek / servis kablosu | Z5 | Pano ayarı yapılırsa evet | "Kilitsiz USB" riski |

## 2 · Yazılım / firmware

| # | Varlık | Not |
| --- | --- | --- |
| Y1 | Kumanda panosu koruma rölesi / kontrolcü yazılımı | Sürümü doğrulanacak |
| Y2 | Dizel kontrol ünitesi firmware | Tedarikçisi doğrulanacak |
| Y3 | S Plus Connect kutusu firmware + işletim sistemi | SBOM zorunlu (EP 09) |
| Y4 | Bulut platformu (sunucu, veritabanı, bildirim servisi) | |
| Y5 | Mobil uygulama (iOS / Android) | |
| Y6 | Servis yazılımı (dizüstüdeki ayar aracı) | Varsa doğrulanacak |

## 3 · Sertifika / anahtar

| # | Varlık | Not |
| --- | --- | --- |
| S1 | Kutu cihaz sertifikası (TLS istemci) | Her kutuya ayrı |
| S2 | Güncelleme imza anahtarı | En kritik anahtar: ele geçerse tüm filo etkilenir |
| S3 | Bulut TLS sertifikası | |
| S4 | VPN / jump server anahtarları | |
| S5 | Mobil bildirim servisi anahtarları | |

## 4 · Dış bağlantı

| # | Bağlantı | Yön |
| --- | --- | --- |
| B1 | Kutu → bulut (4G, TLS) | Sadece dışarı |
| B2 | Pano kuru kontakları → BMS | Tek yönlü |
| B3 | Servis → jump server → VPN | İçeri, süre sınırlı |
| B4 | Bulut → mobil uygulama bildirimleri | Dışarı |
| B5 | Güncelleme sunucusu → kutu | İçeri (imzalı) |
| B6 | Bulut → bayi / servis paneli | Dışarı |

## 5 · Hesaplar

| # | Hesap | Not |
| --- | --- | --- |
| H1 | Bina sahibi / yöneticisi (uygulama) | Okuma |
| H2 | Bina teknik personeli | Okuma + test onayı |
| H3 | Standart Pompa servis teknisyeni | Kişisel, MFA |
| H4 | Bayi teknisyeni | Kişisel, MFA, sadece kendi müşterileri |
| H5 | Platform yöneticisi (Standart Pompa) | Ayrıcalıklı, ayrı onay |
| H6 | Kutu yerel servis hesabı | Varsayılan parola olmamalı |
| H7 | Pano anahtarı (fiziksel "hesap") | Kime verildiği kayıtlı olmalı |

## 6 · Kritik veri akışı

| # | Veri | Nereden → nereye | Neden kritik |
| --- | --- | --- | --- |
| V1 | Alarm / pompa çalışıyor / otomatik mod | Pano → kutu → bulut → telefon | Gecikirse arıza yangına kadar gizli kalır |
| V2 | Haftalık test sonucu | Pano → kutu → bulut → rapor | Yönetmelik ve sigorta kanıtı |
| V3 | Basınç set değeri değişikliği | Pano → kutu (olay olarak) | Sabotaj belirtisi |
| V4 | Firmware güncellemesi | Sunucu → kutu | Tedarik zinciri saldırı yolu |
| V5 | Servis oturum kayıtları | Jump server → arşiv | CRA olay kanıtı |
| V6 | Müşteri ve bina bilgileri | Bulut | KVKK kapsamında kişisel veri |
