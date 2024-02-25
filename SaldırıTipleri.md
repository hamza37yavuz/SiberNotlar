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

## VLAN HOPING SALDIRISI:

__*TRUNK MOD NEDİR*__

Saldırı tiplerine ve tanımlamalarına geçmeden önce trunk modunun ne işe yaradığından bahsedelim. "Trunk modu" (trunk mode), bilgisayar ağlarında kullanılan bir terimdir ve genellikle Ethernet anahtarlarında ve yönlendiricilerinde bulunur. Bu mod, ağ cihazının belirli bir portunun birden fazla VLAN (sanal yerel ağ) trafiğini taşımasını sağlar. Trunk modu, VLAN tabanlı ağlarda ağ trafiğinin yönetimini kolaylaştırmak için kullanılır. Özellikle büyük ağlarda departmanlara ayrılmış ağ trafiğini yönetmek için kullanılır.

Trunk modu, IEEE 802.1Q veya ISL (Inter-Switch Link) gibi protokollerle etiketlenmiş VLAN trafiğini taşır. Bu etiketler, her paketin hangi VLAN'a ait olduğunu belirtir ve alıcı cihazda doğru şekilde yönlendirilmesini sağlar.

Trunk modu, belirli bir portun birden fazla VLAN'a ait trafiği iletebilmesini sağlar. Bu, aynı fiziksel bağlantı üzerinden farklı VLAN'lara ait verilerin taşınabilmesini sağlar. 

Vlan Hoping saldırısının 3 farklı çeşidi vardır:

### SWITCH SPOOFING
Özellikle CISCO Switch'lerde DTP (Dynamic Trunk Protokol) isimli protokol bulunur. Bu protokol şu şekilde işler switch'in belirli bir portuna bağlanan diğer switch trunk moda alınırsa switch bağlantı sağlanan o portu trunk moda çeker. Bu bağlantıyı yeni bir VLAN olarak tanımlar. Bu protokol kötü niyetli kullanıcılara yeni bir kapı açıyor. Saldırgan switch'in bir portuna bağlanıyor bilgisayarını swtich olarak göstererek bağlantı portunu trunk moda çekiyor. Sonrasında yeni bir VLAN oluşturma yetkisine VLAN değiştirme yetkisine sahip oluyor. Örneğin server VLAN'ına bağlanma imkanını elde ediyor.

### DOUBLE TAGGING ATTACK
Saldırgan, cihazını swith gibi yapılandırıyor. IEEE 802.1Q standardına uygun olarak VLAN etiketlerini çift olarak etiketler. Bu şekilde, saldırgan kendi etiketini (outer tag) kullandıktan sonra hedef VLAN'ın etiketini (inner tag) ekler. Bu şekilde, saldırgan fiziksel ağın bir parçasıymış gibi görünür ve hedef VLAN'a erişebilir.

### NATIVE VLAN EXPLOITATION:
Bilgisayar ağlarında, VLAN'lar (Sanal Yerel Ağlar) ağ trafiğini segmente etmek ve yönetmek için kullanılır. Cisco Switch'ler gibi birçok ağ cihazı, VLAN trafiğini yönlendirmek için IEEE 802.1Q protokolünü kullanır. Bu protokolde, VLAN etiketleriyle işaretlenmiş paketler ağ üzerinde taşınır. Cisco Switch'lerde, "native VLAN" olarak adlandırılan özel bir VLAN bulunur. Bu VLAN, ağ cihazlarının VLAN etiketi bulunmayan trafiği taşımasını sağlar. Genellikle, switch yapılandırması varsayılan olarak bu yerel VLAN olarak tanımlanır. Saldırgan bu yapıyı kullanır ve fiziksel olarak erişebildiği bir switch'e bağlanarak yerel VLAN üzerinden trafiği dinleyebilir hatta etkileyebilir. Daha da kötüsü, saldırganlar yerel VLAN üzerinden trafiği yönlendirebilir ve ağdaki diğer cihazlarla iletişim kurabilir.


## DHCP SALDIRILARI

Öncelikle DHCP'nin nasıl çalıştığını inceleyelim sornasında saldırı tiplerini açıklayalım.

DHCP (Dynamic Host Configuration Protocol), ağdaki cihazlara IP adresleri ve diğer ağ yapılandırma bilgilerini otomatik olarak sağlamak için kullanılan bir iletişim protokolüdür. DHCP sunucuları, ağdaki cihazlara dinamik olarak IP adresi tahsis eder ve bu cihazlara gerekli diğer ağ yapılandırma bilgilerini sağlar. DHCP, ağ yöneticilerinin IP adresi tahsisini otomatikleştirmesini ve ağ yapılandırmasını kolaylaştırmasını sağlar.

CLIENT ------> SWITCH --------> DHCP SERVER

Genel olarak, DHCP işleyişi şu adımları izler:

DHCP Discover (Keşif): Yeni bir cihaz ağa bağlandığında veya IP adresini yenilemek istediğinde, DHCP istemcisi (genellikle bilgisayar veya diğer ağ cihazları) ağdaki DHCP sunucularını keşfetmek için bir DHCP Keşif iletişi yayınlar.

DHCP Offer (Teklif): DHCP sunucuları, DHCP Keşif mesajını alır ve mevcut IP adreslerinden birini veya bir dizi IP adresini ve diğer ağ yapılandırma bilgilerini içeren bir DHCP Teklif mesajıyla yanıt verir.

DHCP Request (İstek): İstemci, DHCP Teklif mesajını alır ve sunucudan belirli bir IP adresini talep etmek için bir DHCP İstek mesajı gönderir.

DHCP Acknowledge (Doğrulama): DHCP sunucusu, istemcinin isteğini doğrular ve belirtilen IP adresini tahsis eder. Ardından, DHCP İstemcisine bir DHCP Onay mesajı gönderir. İstemci bu onayı aldığında, ağ yapılandırması tamamlanır ve istemci ağa katılır.

### *__DHCP Saldırı Türleri__*

*__DHCP Spoofing (Sahte DHCP):__*

Saldırgan, ağdaki DHCP sunucusunun yanıtlarını taklit ederek DHCP iletişimini manipüle eder. Discover paketi sonrası saldırganın paketi istemciye ilk yanıtı verir. Saldırgan kullanıcıya kendisinin gateway olduğu bir IP adresi verebilir. Ya da saldırgan kendi bilgisayarını DNS Server olarak gösterme şansı yakalayabilir. 
Bu saldırı, ağdaki istemcilerin güvenliğini ve veri gizliliğini tehlikeye atar. Bu durumu DHCP Snooping ile engelleyebiliriz. Switch'in DHCP portu güvenilir port olarak istemcilerin portları ise güvensiz port olarak ayarlanabilir. Bu durumda discover paketi sonrası güvensiz portlar arası iletişim olmaması sağlanır. Aynı zamanda bu ayarlamalar sırasında VLAN bazında bir kullancının kaç discover paketi atabileceğine limit konulabilir. Bu limit sayesinde DHCP Starvationa da engellenebilir.

*__DHCP Starvation (DHCP Açlığı):__*

Saldırgan, DHCP sunucusuna ağdaki tüm IP adreslerini tüketmesi için sürekli sahte mac adreslerini değiştirir. Devamlı IP adresi isteyerek VLAN'daki tüm IP'leri doldurur.
Bu şekilde, mevcut IP adresleri tükendiğinde, yeni cihazlar IP adresi alamaz ve ağa katılamazlar.
Ağdaki hizmetin kesilmesine neden olur ve ağ erişimini engeller. Switch'lerde yapılan port güvenliği işlemleri bu saldırının önüne geçebilir. 


*__DHCP Rogue Server (Sahte DHCP Sunucusu):__*

Saldırgan, mevcut DHCP sunucularına benzeyen sahte bir DHCP sunucusu kurar. Burada sunucunun kendisi taklit edilir. Eğer sunucunun verdiği yanıtlar taklit edilirse bu DHCP Spoofing olur.
Bu sahte sunucu, ağdaki istemcilere yanlış IP adresleri veya zararlı yapılandırma bilgileri sağlar.
Ağ trafiğini yönlendirir ve saldırganın kontrolü altına alınmış bir ortam yaratır. Bu durumun önüne geçmek için DHCP Snooping, DHCP Authentication ve Port Security yapılabilir.

## ARP SALDIRISI:

Öncelikle ARP nasıl çalışıyor onu bilmemiz gerekir. Kısaca bahsedelim: Bir ağda bulunan x cihazı y cihazının bilgilerini bilmiyor ve o cihazla iletişim kurmak istiyor. Bu durumda aradıağı cihazın cevap vermesi için ağda bir arp paketi yayımlıyor. Bu paketin içerisinde yer alan MAC adresi bir cihazla eşleşiyor sonrasında y cihazı arananın kendisi olduğunu fark ederek x cihazına geri paket gönderiyor. x cihazı da gelen paket üzerine y cihazının bilgilerini ARP tablosuna kaydediyor. Peki saldırganlar nasıl bu protokolden istifade ediyor açıklayalım:

__*ARP Spoofing (ARP Zehirlenmesi):*__

ARP zehirlenmesi, saldırganların ağdaki diğer cihazları yanıltmak için sahte ARP cevapları gönderdiği bir saldırı türüdür. 
A bilgisayarı yönlendiriciye bağlanmak ve internete çıkmak için bir ARP paketi yayımlar.
Bu paket saldırgan ve yönlendirici dahil herkese iletilir. Saldırgan daha öncesinde yönlendiriciyi kendi ARP tablosuna kaydetmiştir ve bilgisine sahiptir.
Bu sayede saldırgan yönlendiricinin göndereceği cevabı taklit edebilir. Yönlendiriciden önce a bilgisayarına kendi bilgilerini gönderir.
Kendine a bilgisayarından gelen paketleri tekrar yönlendiriciye yollar. Bu sayede a bilgisayarı internete çıkmış olur.

Kısaca saldırganlar, hedef cihazları kendi MAC adresleriyle ilişkilendirmek için sahte ARP yanıtları gönderirler. Böylece, ağdaki diğer cihazlar, aslında saldırganın cihazının MAC adresine doğru IP adresi eşleştirmiş olurlar.

ARP zehirlenmesi, saldırganların ağ trafiğini dinlemesine, izlemesine ve hatta manipüle etmesine olanak tanır. Örneğin, saldırganlar, kullanıcı adları, şifreler veya diğer hassas bilgiler gibi ağ trafiğinde iletilen bilgilere erişebilirler.

Bu saldırıya ve aşağıdaki diğer saldırılara önlem olarak switch üzerinde dhcp snooping yapılandırması yapılmalıdır. Bu sayede IP-MAC eşleştirmeleri yapılır. Şüpheli paketler ARP inspection sayesinde engellenir.

__*ARP Cache Poisoning (ARP Önbellek Zehirlenmesi):*__

ARP önbellek zehirlenmesi, saldırganların hedef cihazların ARP önbelleklerini manipüle ederek ağ trafiğini yönlendirdiği bir saldırı türüdür. Bu saldırı, ağdaki diğer cihazların ARP tablolarına yanlış eşleştirmeler ekleyerek gerçekleştirilir.

Saldırganlar genellikle ağa katılan bir cihazın ARP yanıtlarını yanlış yönlendirirler. Örneğin, saldırgan, hedef cihazın IP adresine kendi MAC adresini ekleyerek, ağ trafiğinin saldırganın kontrolü altına girmesini sağlar. Bu durumda, hedef cihaz, doğru hedefe gönderilmesi gereken veriyi saldırganın cihazına yönlendirecektir.

Bu tür bir saldırı, saldırganın ağdaki veriyi izlemesine ve hatta manipüle etmesine olanak tanır. Örneğin, saldırganlar, hassas verileri ele geçirmek veya iletişimi engellemek için bu yöntemi kullanabilirler.

__*ARP Flood Attack (ARP Taşkını Saldırısı):*__

ARP taşkını saldırısı, ağdaki cihazların ARP önbelleklerini doldurarak ağ trafiğini engellediği veya etkisiz hale getirdiği bir saldırı türüdür. Bu saldırı, saldırganların ağa büyük miktarda sahte ARP istekleri göndererek gerçekleştirilir.

Saldırganlar, ağdaki diğer cihazların ARP önbelleklerini doldurarak, bu cihazların doğru hedeflere yönlendirilmesini engellerler. Bu durumda, ağ trafiği normal şekilde işlenemez ve ağ performansı ciddi şekilde etkilenir.

ARP taşkını saldırıları genellikle ağ kaynaklarını tüketerek ağdaki iletişimi durdurmayı veya etkisiz hale getirmeyi amaçlar. Bu tür saldırılar, ağın kullanılabilirliğini ciddi şekilde etkileyebilir ve hizmet kesintilerine neden olabilir.

