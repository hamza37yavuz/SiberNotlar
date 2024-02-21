# AĞ GÜVENLİĞİ TEMELLERİ SALDIRI TİPLERİ

## MAC TABLE ATTACK (MAC TABLO SALDIRISI):

### MAC TABLOSU:
MAC (Medya Erişim Kontrolü) tablosu, bir ağ cihazının ağda diğer cihazlarla iletişim kurmak için kullandığı fiziksel adreslerin listesidir. Bu tablo, cihazların IP adreslerini fiziksel MAC adreslerine eşler.

### SALDIRI TİPLERİ:
MAC Tablosu Saldırıları, ağdaki cihazların MAC tablolarını hedef alır. Bu saldırıların çeşitli tipleri vardır:

__*MAC Flooding (MAC Taşma):*__ Saldırgan, ağdaki switch gibi cihazların MAC tablolarını doldurmak için yüksek miktarda sahte MAC adresi paketi gönderir. Bu, switch'in MAC tablosunun dolmasına ve meşru cihazların iletişiminin engellenmesine neden olabilir.

__*MAC Spoofing (MAC Sahteciliği):*__ Saldırgan, meşru bir cihazın MAC adresini taklit ederek ağdaki diğer cihazlarla iletişim kurar. Böylece, saldırganın veri trafiği izlenebilir veya değiştirilebilir.

### Korunma Yöntemleri:
MAC Tablosu Saldırılarına karşı alınabilecek bazı önlemler şunlardır:

__*Port Security (Port Güvenliği):*__ Ağ cihazlarında port güvenliği ayarlarını yapılandırmak, yalnızca belirli MAC adreslerinin belirli portlardan iletişim kurmasına izin verir. Bu işlem manuel olarak yapılabilir. Her bir port için sınırlı sayıda MAC adresine izin verilir. Sticky olarak da yapılabilir.
Peki ihlal durumlarında ne olur:

SHUT DOWN: Direkt port üzerinden bilgi akışı durdurulur portu tekrar manuel olarak açmak gerekir.

RESTRİCT: İhlali gerçekleştiren MAC adresi engellenir ama diğer ciazlardan veri akışı devam eder. İhlali gerçekleştiren cihazın logu kaydedilir.

PROTECT: İhlal gerçekleşse bile port üzerinde kesinti yapılmaz. Bu durum çok kritik hizmetler sunulan portlarda kullanılır.

Bir mac tablosuna yapılan kayıtlar sonrasında o mac adresi ne zaman tablodan silinir. Bu durumda Aging Time (Yaşlanma Zamanı) adını verdiğimiz kural takip edilir:

Absolute (Kesin) durumuna göre belirlenen süreyi dolduran MAC adresi aktif de olsa tablodan silinir.

Inctivity (Bağlı olmama) durumuna göre ise cihazın bir ağda aktif olmadan belirli süre bulunması sonrasında MAC adresi tablodan silinir. 

__*MAC Address Filtering (MAC Adres Filtreleme):*__ Yalnızca belirli MAC adreslerinin ağa erişmesine izin veren bir filtreleme politikası uygulamak.

__*Network Monitoring (Ağ İzleme):*__ Ağ trafiğini sürekli olarak izleyen ve anormal aktiviteleri tespit eden bir ağ izleme sistemi kullanmak.
