# Evidence Pack — 15 Başlık Durum Tablosu

"Yarın denetçi geldi — masaya hangi dosyaları koyacaksınız?"

Durum merdiveni sunumdaki kanıt hiyerarşisidir: **Yok → Taslak → Var → Doğrulanmış.** "Bugün" sütunu, kamuya açık bilgilere göre tahmindir ve firmadan doğrulanmalıdır. "Bu çalışmadan sonra" sütunu, föylerin ürettiği taslakları gösterir.

**Sonuç:** Bugün 15 başlığın en fazla 2'si "Var" seviyesinde (emniyet fonksiyonları ve test kayıtları, NFPA 20 belgeleri sayesinde). Föylerle 9 başlık "Taslak"a çıkıyor; 5 başlık (08, 09, 11, 12, 14) hâlâ "Yok", çünkü bunlar için ürünün kendisi henüz yok.

| EP | Başlık | Bugün (tahmin) | Bu çalışmadan sonra | Kaynak föy / dosya | Sıradaki adım |
| --- | --- | --- | --- | --- | --- |
| 01 | Asset Inventory | Yok | Taslak | [01-varlik-envanteri.md](01-varlik-envanteri.md) | Pano içi elektronik ve firmware sürümleri firmadan alınır |
| 02 | Network Architecture | Yok | Taslak | Lab 4, [08-mimari.md](08-mimari.md) | Kablolama şemasıyla tek yönlü bağlantı kanıtlanır |
| 03 | Safety Functions | Var | Taslak (güncellenmiş) | Lab 1, Lab 7 | Siber bağımlılıklar mevcut emniyet dokümanına eklenir |
| 04 | Cyber Risk Assessment | Yok | Taslak | Lab 3 | Grup ve firma ile puanlar kalibre edilir |
| 05 | Zone & Conduit | Yok | Taslak | Lab 2 | Pilot sahada doğrulanır |
| 06 | Remote Access Procedure | Yok | Taslak | Lab 2 Görev B, Lab 4 | Yazılı prosedür + onay akışı |
| 07 | User/Role Matrix | Yok | Taslak | Envanter "Hesaplar" | Rollere izin tablosu çıkarılır |
| 08 | Software/Firmware Inventory | Yok | Yok | — | Pano ve dizel ünitesi sürümleri toplanır |
| 09 | SBOM | Yok | Yok (şablon) | Lab 5 | Kutu tasarlanırken otomatik SBOM üretimi |
| 10 | Vulnerability Records | Yok | Taslak (karar akışı) | Lab 5 | Açık bildirim politikası yayımlanır |
| 11 | Patch/Update Records | Yok | Yok | Lab 5 | İmzalı güncelleme altyapısı kurulur |
| 12 | Backup & Restore | Yok | Yok | — | Pano ayarlarının yedeği ve geri yükleme prosedürü |
| 13 | Incident Response | Yok | Taslak | Lab 6 | Tatbikat yapılır, RACI imzalanır |
| 14 | Change Management | Yok | Yok | — | Pano ayar değişikliği için iş emri + kayıt formu |
| 15 | Verification/Test | Var (NFPA 20 fabrika ve kabul testleri) | Var | Katalog | Siber güvenlik testleri (sızma testi) eklenir |

**Hedef (sunumdaki kural):** Her başlıkta bir basamak yukarı. 90 günlük plan bunu takvime bağlar: [03-raci-90-gun.md](03-raci-90-gun.md).
