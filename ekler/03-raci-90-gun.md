# Safety 4.0 RACI ve 90 Günlük Plan

## RACI — "kim?" sorusu

R = yapan · A = nihai sorumlu (tek) · C = görüşü alınan · I = bilgilendirilen. Roller sunumdaki yedi sütundur; Standart Pompa organizasyonuna uyarlanmıştır ve firmayla doğrulanmalıdır.

| İş | İş (Satış/Pazarlama) | Tasarım (Ar-Ge) | OT (Pano/Otomasyon) | IT | Safety | Servis | Yönetim |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Asset inventory | C | R | R | C | C | C | **A** |
| Remote access | I | C | R | R | C | C | **A** |
| Patch / update | I | R | C | C | C | R | **A** |
| Safety change (pano ayarı) | I | C | C | I | R | C | **A** |
| Incident | C | C | R | R | C | R | **A** |
| Risk assessment | C | R | R | C | R | C | **A** |
| SBOM ve açık yönetimi | I | R | C | R | I | I | **A** |
| S Plus Connect abonelik ve müşteri bildirimi | R | I | I | C | I | R | **A** |
| CRA otorite bildirimi | I | C | C | C | C | I | **A** |

Sunumdaki kural: **A'sı boş satır = sahipsiz iş → 90 günlük plana girer.** Son üç satır sunumdaki tabloda yoktu; bu ürün için eklendi. Yönetim içinde tek bir "ürün güvenliği sorumlusu" atanması önerilir.

## 90 günlük plan

| Hafta | İş | Evidence Pack | Sorumlu (A) | Çıktı |
| --- | --- | --- | --- | --- |
| 1–2 | Ürün güvenliği sorumlusunu ata, RACI'yi imzalat | 07 | Yönetim | İmzalı RACI |
| 1–3 | Pano tiplerinin iç yapısını ve firmware sürümlerini topla | 01, 08 | Yönetim (R: OT) | Envanter v1 |
| 2–4 | Kutu için "sadece okur" tasarım gereksinimini yaz, kablolama şemasını çiz | 02, 05 | Yönetim (R: Tasarım) | Gereksinim dokümanı |
| 3–6 | Uzak erişim prosedürü: jump server, MFA, kişisel hesap, oturum kaydı | 06 | Yönetim (R: IT) | Prosedür v1 |
| 4–8 | Kutu prototipi; SBOM'u derleme sürecinde otomatik üret | 09 | Yönetim (R: Tasarım) | Prototip + SBOM |
| 5–8 | Pano ayar değişikliği için iş emri ve kayıt formu | 12, 14 | Yönetim (R: Safety) | Değişiklik formu |
| 6–9 | Açık bildirim politikası ve açık kayıt şablonu yayımla | 10 | Yönetim (R: IT) | Web'de politika |
| 8–10 | Olay müdahale tatbikatı (Lab 6 senaryosu) | 13 | Yönetim (R: OT + Servis) | Tatbikat raporu |
| 9–12 | 3–5 pilot sahada kurulum ve doğrulama | 02, 05, 15 | Yönetim (R: Servis) | Pilot raporu |
| 12–13 | Evidence Pack durumunu yeniden değerlendir | Tümü | Yönetim | Durum tablosu v2 |

**90 gün sonunda hedef:** EP 01, 02, 05, 06, 07, 13 "Var"; EP 09, 10, 14 en az "Taslak".
