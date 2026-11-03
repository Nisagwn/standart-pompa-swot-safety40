# S Plus Connect — Gelir Modeli ve Kaba Hesap

> **Uyarı:** Bu sayfadaki bütün fiyat ve maliyetler **örnek varsayımdır**; firma fiyat açıklamadığı için bir karar modeli göstermek amacıyla seçilmiştir. Gerçek rakamlar firmadan alındığında tablo yeniden hesaplanmalıdır.

## Gelir kalemleri

| Kalem | Kime | Nasıl |
| --- | --- | --- |
| S Plus Connect kiti | Yeni yangın pompa seti alan müşteri | Set fiyatına opsiyon olarak eklenir |
| Sonradan takma kiti | Sahada eski seti olan müşteri | Servis ziyaretinde takılır |
| Yıllık abonelik | Bina sahibi / tesis | İzleme, bildirim, otomatik test raporu |
| S Plus bakım paketi (mevcut) | Bina sahibi | Abonelikle birlikte paketlenir; ziyaret sayısı korunur |
| Evidence Pack hazırlama hizmeti | Hastane, AVM, fabrika | Proje bazlı danışmanlık |

## Örnek varsayımlar

| Varsayım | Değer | Not |
| --- | --- | --- |
| Kit satış fiyatı | 40.000 TL | varsayım |
| Kit maliyeti (donanım + montaj) | 20.000 TL | varsayım |
| Yıllık abonelik | 18.000 TL / saha | varsayım; ayda 1.500 TL |
| Saha başına yıllık değişken gider (SIM, bulut, destek) | 3.000 TL | varsayım |
| Platform sabit gideri (3 kişilik ekip + bulut + güvenlik testi) | 6.000.000 TL / yıl | varsayım |

## Başa baş hesabı

- Saha başına yıllık abonelik katkısı = 18.000 − 3.000 = **15.000 TL**
- Kit başına tek seferlik katkı = 40.000 − 20.000 = **20.000 TL**
- Sadece abonelikle başa baş = 6.000.000 / 15.000 = **400 abone saha**

| Senaryo | Abone saha | Yıllık abonelik katkısı | Yeni kit (yıl) | Kit katkısı | Sabit gider | Sonuç |
| --- | --- | --- | --- | --- | --- | --- |
| Temkinli | 150 | 2,25 milyon TL | 100 | 2,0 milyon TL | 6,0 milyon TL | −1,75 milyon TL |
| Beklenen | 400 | 6,0 milyon TL | 200 | 4,0 milyon TL | 6,0 milyon TL | +4,0 milyon TL |
| İyimser | 1.000 | 15,0 milyon TL | 400 | 8,0 milyon TL | 6,0 milyon TL | +17,0 milyon TL |

## Yorum

- Model abonelik sayısına çok duyarlı. Kritik soru: **sahada kaç yangın pompa seti var ve bunların kaçı S Plus müşterisi?** Mevcut S Plus müşterileri ilk ve en kolay abone adayı.
- Firmanın tahmini yıllık satışı yaklaşık 2 milyar TL olduğu için beklenen senaryodaki 10 milyon TL'lik ek katkı küçük görünür; asıl değer **tekrarlayan gelir, müşteri bağlılığı ve AB'de CRA uyumlu ürünle fark** yaratmaktır.
- Armstrong da benzer şekilde kiti ve ilk yıl aboneliğini pompayla paket satıyor; ilk yıl ücretsiz abonelik denemeye değer bir satış taktiği.
