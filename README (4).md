# HYDRA Makine Analizi — Safety 4.0

Yazılım Mühendisliği Güncel Konular dersi kapsamında, **TOLKAR HYDRA Endüstriyel Yıkama ve Sıkma Makinesi** üzerinden hazırlanan işlevsel emniyet, endüstriyel siber güvenlik ve yapay zekâ güvenliği analizleri.

## Amaç

Siber güvenlik olaylarının makinenin çalışmasına ve insan güvenliğine etkisini senaryolar üzerinden değerlendirmek; emniyet fonksiyonlarını, güvenli uzak erişim gereksinimlerini ve olay müdahale adımlarını belgelemek.

## İncelenen Makine

Örnek makine, dönen tambur ve yüksek devirli sıkma işlemi içeren HYDRA endüstriyel yıkama ve sıkma makinesidir. Analizde kapı kilidi, sıfır hız izleme, acil durdurma (E-stop), emniyet kontrol sistemi ve Güvenli Tork Kesme (STO) fonksiyonları ele alınır.

> Belgelerdeki “şişeleme tabanlı” ve “paketleme tabanlı” ifadeleri kullanılan laboratuvar föylerinin sürümlerini belirtir. Her iki sürümde de analiz edilen örnek makine HYDRA yıkama ve sıkma makinesidir.

## Çalışmanın Kapsamı

| Laboratuvar | Konu | Hazırlanan çıktı |
| --- | --- | --- |
| 1 | Emniyet fonksiyonları ve dijital bağımlılıklar | Safety Function Map |
| 2 | Ağ bölgeleri ve kontrollü geçişler | Zone / Conduit Diagram |
| 3 | Siber müdahalenin fiziksel zarara dönüşmesi | Risk Register |
| 4 | Güvenli uzak bakım erişimi ve emniyet bağımsızlığı | Secure Architecture |
| 5 | SBOM, CVE değerlendirmesi ve yama kararları | Vulnerability Decision |
| 6 | Yetkisiz servis erişimi ve olay müdahalesi simülasyonu | Incident Workflow |
| 7 | Yapay zekâ hatalarında güvenli davranış | AI Fail-Safe Decision |

## Belgeler

| Dosya | İçerik |
| --- | --- |
| `HYDRA_Sisleme_Genel_Surumu_5sf (2).docx` | Genel sürüm laboratuvar föyleri ve HYDRA üzerinden önerilen yanıtlar |
| `HYDRA_Paketleme_Surumu_5sf (1).docx` | Paketleme tabanlı föylerin HYDRA örneğine uyarlanmış sürümü |
| `HYDRA_Sisleme_ve_Paketleme_Lab4-5-6-7.pdf` | Her iki sürüm için laboratuvar 4–7 çalışmalarının birleştirilmiş PDF belgesi |

Dosya adlarındaki `(1)` ve `(2)` ekleri, yüklenen kopyaların adlarının parçasıdır. Depoda dosyalar yeniden adlandırılırsa bu tablo da güncellenmelidir.

## Temel Yaklaşım

- Emniyet fonksiyonlarını normal üretim kontrolünden ve uzak bakım erişiminden bağımsız değerlendirmek.
- Uzak erişimde VPN, çok faktörlü kimlik doğrulama (MFA), ara sunucu (jump server), kişisel hesap ve oturum kaydı kullanmak.
- Ağları bölgelere ayırmak ve geçişleri ihtiyaç duyulan erişimlerle sınırlandırmak.
- Zafiyet kararlarında bileşenin varlığını, etkilenen sürümü ve erişilebilirliği birlikte incelemek.
- Yama öncesinde test, yedekleme ve geri dönüş planı hazırlamak.
- Olay müdahalesinde insan güvenliğini ve dijital kanıtların korunmasını öncelemek.
- Yapay zekâ önerilerini bağımsız emniyet kontrolleri, insan müdahalesi ve güvenli geri dönüş davranışlarıyla değerlendirmek.

## Belgeleri İnceleme

Önce genel veya paketleme tabanlı Word belgesi üzerinden laboratuvar 1–3 incelenebilir. Ardından birleştirilmiş PDF ile laboratuvar 4–7 çalışmaları karşılaştırılabilir. Word belgeleri indirilerek Word veya uyumlu bir uygulamada açılabilir.

## Varsayımlar ve Sınırlar

Bu çalışma eğitim amaçlı bir dokümantasyon çalışmasıdır. Üreticinin teknik dosyası incelenmeden, endüstriyel yıkama ve sıkma makinelerinin tipik yapısı üzerinden hazırlanmıştır.

Ağ yapısı, uzak bakım erişimi, hesap bilgileri, PLr düzeyi, emniyet mimarisi ve yapay zekâ kullanımı gibi ayrıntılar senaryo varsayımlarıdır; HYDRA ürününde doğrulanmış özellik veya zafiyet olarak yorumlanmamalıdır. Belgelerdeki örnek CVE kaydı da gerçek bir zafiyet bildirimi değildir.

Bu depo resmî denetim, uygunluk değerlendirmesi, belgelendirme veya CE uygunluğu kanıtı sunmaz. Olay simülasyonundaki mevzuat başlıkları ve süreler eğitim senaryosunun parçasıdır; güncel hukuki yükümlülükleri doğrulayan bir kaynak olarak kullanılmamalıdır.

## Hazırlayan

**Hilal Gül Arıboğa**  
Fırat Üniversitesi · Yazılım Mühendisliği

## Materyal Kaynağı

Çalışmada, üzerinde **INSPECCO × KRIPTARIUM — Safety 4.0 Bootcamp** başlığı bulunan laboratuvar föyleri temel alınmıştır. Kaynak materyallerin hakları ilgili sahiplerine aittir.
