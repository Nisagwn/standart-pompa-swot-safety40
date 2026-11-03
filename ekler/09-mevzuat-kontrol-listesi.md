# Mevzuat Kontrol Listesi — Bağlantılı Yangın Pompa Seti

> Bu liste eğitim amaçlıdır; hukuki görüş veya uygunluk değerlendirmesi değildir. Hangi mevzuatın hangi ürüne uygulanacağı onaylanmış kuruluş ve hukuk danışmanıyla netleştirilmelidir.

## Takvim

| Tarih | Ne oluyor |
| --- | --- |
| 15.03.2018 | Binaların Yangından Korunması Hakkında Yönetmelik değişikliği (Madde 93 yangın pompaları) yürürlükte |
| 11 Eylül 2026 | CRA: aktif istismar edilen açıklar ve ciddi olaylar için bildirim yükümlülüğü başladı (piyasadaki mevcut ürünler dahil) |
| 20 Ocak 2027 | AB Makine Tüzüğü 2023/1230 uygulanmaya başlar; geçiş dönemi yok |
| 11 Aralık 2027 | CRA'nın ana yükümlülükleri (temel siber güvenlik gereksinimleri, uygunluk değerlendirmesi) tam uygulanır |

Kaynaklar: [McCann FitzGerald](https://www.mccannfitzgerald.com/knowledge/data-privacy-and-cyber-risk/cyber-resilience-act-reporting-obligations-apply-from-11-september-2026), [İrlanda Hükümeti duyurusu](https://www.gov.ie/en/department-of-justice-home-affairs-and-migration/press-releases/cyber-resilience-act-guidelines-published-as-reporting-obligations-come-into-effect/), Safety 4.0 Bootcamp sunumu.

## 1 · Türkiye — Binaların Yangından Korunması Hakkında Yönetmelik

- [ ] Her pompanın ayrı, kilitli kumanda panosu var (Madde 93)
- [ ] Panoda faz hatası, faz sırası ve kumanda fazı hata ışıkları var
- [ ] Her pompanın ayrı basınç anahtarı var; ayarlar kilitlenebilir
- [ ] Tek pompa varsa aynı kapasitede yedek pompa var
- [ ] Dizel yedek yoksa enerji binanın genel sisteminden bağımsız
- [ ] Periyodik kontrol, test ve bakım kayıtları bina sahibi/yöneticisi tarafından yaptırılıyor → **S Plus Connect bu kaydı otomatik tutar**

## 2 · CRA (AB) 2024/2847 — bağlantılı kutu ve yazılımı için

- [ ] Ürün "dijital unsurlu ürün" mü ve hangi sınıfta? (hukuki teyit)
- [ ] Bilinen istismar edilebilir açık olmadan piyasaya arz
- [ ] Güvenli varsayılan yapılandırma (varsayılan parola yok)
- [ ] Yetkisiz erişime karşı koruma (kimlik doğrulama, MFA)
- [ ] Verinin gizliliği ve bütünlüğü (TLS, imza)
- [ ] Veri minimizasyonu (sadece gerekli teknik veri)
- [ ] Erişilebilirlik ve saldırı yüzeyinin küçültülmesi
- [ ] Güvenlikle ilgili olayların kaydı
- [ ] Güvenlik güncellemelerinin destek süresi boyunca sağlanması; destek süresinin ilan edilmesi
- [ ] SBOM'un hazırlanması ve güncel tutulması
- [ ] Koordineli açık bildirim politikası ve iletişim noktası
- [ ] 24 saat erken uyarı / 72 saat bildirim / 14 gün son rapor süreci (Lab 6)

## 3 · AB Makine Tüzüğü 2023/1230 — yangın pompa seti için

- [ ] Kontrol sistemlerinin güvenliği ve güvenilirliği; kötü niyetli müdahale dahil öngörülebilir dış etkilere dayanıklılık
- [ ] Bozulmaya / yetkisiz değişikliğe karşı koruma: emniyet için kritik yazılım ve verinin korunması, müdahalenin kayıt altına alınması
- [ ] Bağlı cihazların (izleme kutusu) emniyet fonksiyonunu tehlikeye atmaması → tek yönlü tasarım
- [ ] Teknik dosyada siber güvenlik risk değerlendirmesinin bulunması → Lab 3, EP 04

## 4 · Telsiz ekipman — 4G modem

- [ ] Kutudaki 4G modem telsiz ekipman sayıldığı için RED kapsamında siber güvenlik gereksinimlerinin (EN 18031 serisi) ve modem tedarikçisinin uygunluk belgelerinin kontrolü (onaylanmış kuruluşla teyit edilmeli)

## 5 · Standartlar

- [ ] NFPA 20 (yangın pompası kurulumu) — mevcut
- [ ] NFPA 25 (test, muayene, bakım) — aylık/yıllık testler; test sıklığı güncel metinden doğrulanmalı
- [ ] IEC 62443 (endüstriyel siber güvenlik; zone/conduit) — Lab 2
- [ ] ISO 13849 / IEC 62061 (emniyet fonksiyonları) — Lab 1
- [ ] ISO/IEC 42001 (yapay zekâ yönetim sistemi) — arıza tahmini eklenirse, Lab 7

## 6 · Türkiye — KVKK

- [ ] Bina ve müşteri bilgileri için aydınlatma metni ve veri işleme sözleşmesi
- [ ] Bulut sunucusunun konumu ve yurt dışı aktarım değerlendirmesi
