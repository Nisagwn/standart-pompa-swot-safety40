# S Plus Connect — Mimari

**Ana ilke:** Veri sadece emniyet bölgesinden dışarı akar. Hiçbir ağ bağlantısı pompayı başlatamaz, durduramaz ya da ayarını değiştiremez.

```mermaid
flowchart LR
  subgraph Z1["Z1 · Emniyet (ağ yok, kilitli)"]
    BA["Basınç anahtarları"] --> PANO["Kumanda panoları<br/>(elektrik / dizel / jokey)"]
    PANO --> POMPA["Pompalar<br/>Safe state: ÇALIŞIR"]
  end
  subgraph Z2["Z2 · İzleme"]
    KUTU["S Plus Connect kutusu<br/>(sadece okur)"]
  end
  subgraph Z3["Z3 · Bina"]
    BMS["BMS / yangın alarm paneli"]
  end
  subgraph Z4["Z4 · Bulut"]
    BULUT["S Plus platformu"] --> APP["Mobil uygulama<br/>+ servis paneli"]
  end
  subgraph Z5["Z5 · Servis"]
    TEK["Teknisyen"] --> JUMP["Jump server<br/>VPN + MFA + kayıt"]
  end
  PANO -- "kuru kontak, tek yönlü" --> KUTU
  PANO -- "kuru kontak, tek yönlü" --> BMS
  KUTU -- "4G, TLS, sadece dışarı" --> BULUT
  JUMP -- "süre sınırlı" --> BULUT
  TEK -. "sadece fiziksel, anahtarla" .-> PANO
```

## Bileşenler ve sınırlar

| Bileşen | Yapar | Yapamaz |
| --- | --- | --- |
| Kumanda panoları | Pompayı otomatik/elle çalıştırır, alarmları üretir | Ağdan komut almaz |
| S Plus Connect kutusu | Kuru kontakları okur, olay ve test kaydını buluta yollar, bağlantı kesilince alarm üretir | Panoya sinyal yazamaz (fiziksel olarak çıkış yok) |
| BMS | Durumu gösterir | Pompayı çalıştıramaz / durduramaz (katalog önerisi) |
| Bulut | Bildirim, rapor, arıza tahmini | Kutuya komut göndermez; sadece imzalı güncelleme |
| Jump server | Kayıtlı, süre sınırlı servis erişimi | Kalıcı açık değildir |

## Güvenlik özellikleri (CRA ve IEC 62443 ile eşleşme)

| Özellik | Karşıladığı gereksinim |
| --- | --- |
| Varsayılan parola yok, cihaza özel sertifika | Güvenli varsayılan yapılandırma |
| Sadece dışarı giden TLS, gelen port kapalı | Saldırı yüzeyini küçültme |
| İmzalı güncelleme, SBOM | Güvenlik güncellemeleri ve açık yönetimi |
| Olay ve oturum kaydı | Kayıt ve izleme, olay müdahalesi |
| "Kutu sustu" alarmı | Erişilebilirlik / kesintinin fark edilmesi |
| Tek yönlü kablolama | Emniyet fonksiyonunun bağımsızlığı (Lab 4) |
