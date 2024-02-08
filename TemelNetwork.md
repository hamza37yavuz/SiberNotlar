<a name="top"></a>

---
<h1 align="center"> TEMEL AĞ EĞİTİMİ</h1>


Network: En az iki cihazın birbiri ile haberleşmesi Network olarak adlandırılır

__*Ağ Bileşenleri:*__
Switch, Router, Access point, Modem, Kablo

### SWITCH:
Ağ içerisinde bulunan cihazlar birbiri ile haberleşmesi ve veri transferi yapılmasını sağlayan, ağ anahtarı olarak da bilinen bir ağ cihazıdır. 

__*Yönetilebilir Switch:*__ WLAN tanımı oluşturabilme, portların ayarlarını yapabilme, ağ trafiğini izleyebilme gibi özellikleri bulunan, layer 2 ve layer 3 olarak iki katmanda çalışan bir switch türüdür. Genelde layer 3 switchler, routing yapabilme özelliğine sahiptir. 

__*Yönetilemez Switch:*__ WLAN tanımı oluşturama, portların ayarlarını yapama, ağ trafiğini izleyememe gibi özellikleri bulunmayan, sadece layer 2 katmanında çalışan bir switch türüdür. Routing yapamaz.

| Özellik | Yönetilebilir Switch | Yönetilemez Switch |
|---|---|---|
| Yönetim | **Var** | **Yok** |
| Katman | **Layer 2 veya Layer 3** | **Layer 2** |
| Routing | **Var (Layer 3 switchlerde)** | **Yok** |
| WLAN Tanımı | **Var** | **Yok** |
| Port Ayarları | **Var** | **Yok** |
| Ağ Trafiği İzleme | **Var** | **Yok** |
| Güvenlik | **Daha yüksek** | **Daha düşük** |
| Fiyat | **Daha yüksek** | **Daha düşük** |

### ROUTER:
Bir kullanıcının internete bağlanabilmesi için gerekli yönlendirmeyi sağlar. Genel yapı şu şekildedir: WAN -> Router-> Switch -> User

Router üzerinde her port farklı bir ağ barındrırır. Genellikle ISP'ler tarafından kullanılır.

**Static Routing:** Statik yönlendirme, bir yönlendiricinin yönlendirme tablosuna manuel olarak rotalar eklediği bir yönlendirme türüdür. Statik rotalar, yönlendirici tarafından değiştirilemez veya güncellenemez.

**Dinamik Routing:**Dinamik yönlendirme, yönlendiricilerin ağdaki diğer yönlendiricilerden yönlendirme bilgilerini öğrendiği bir yönlendirme yöntemidir. Bu, yönlendiricilerin kendi başlarına ağdaki tüm ağları ve ağ yollarını öğrenmesine gerek olmadığı anlamına gelir.

Dinamik yönlendirme, statik yönlendirmeye göre aşağıdaki avantajlara sahiptir:

Esneklik: Dinamik yönlendirme, ağ topolojisindeki değişikliklere otomatik olarak uyum sağlayabilir.

Etkinlik: Dinamik yönlendirme, ağda mevcut olan en iyi yolu otomatik olarak seçebilir.

Otomatik kurulum: Dinamik yönlendirme, yönlendiricilerin ağda kendi başlarına yapılandırılmasına olanak tanır.

Dinamik yönlendirme, aşağıdaki protokolleri kullanır:

RIP (Routing Information Protocol): RIP, en basit dinamik yönlendirme protokolüdür. RIP, yönlendirme bilgilerini hop mesafesi olarak bilinen bir ölçüm kullanarak hesaplar.

OSPF (Open Shortest Path First): OSPF, daha karmaşık bir dinamik yönlendirme protokolüdür. OSPF, yönlendirme bilgilerini maliyet olarak bilinen bir ölçüm kullanarak hesaplar.

EIGRP (Enhanced Interior Gateway Routing Protocol): EIGRP, OSPF'ye benzer bir dinamik yönlendirme protokolüdür. EIGRP, yönlendirme bilgilerini maliyet ve hop mesafesi gibi birden çok faktörü kullanarak hesaplar.

Uzaklığın hesaplanması, dinamik yönlendirme protokollerinin temel bir özelliğidir. Hop mesafesi ve maliyet, uzaklığı hesaplamak için kullanılan iki yaygın ölçümdür.

Hop mesafesi, bir paketin bir yönlendiriciden diğerine geçmesi gereken sayısıdır. Hop mesafesi, bir paketin hedefe ulaşmak için kat etmesi gereken mesafeyi temsil eder.

Maliyet, bir yönlendiriciden diğerine geçmenin maliyetini temsil eder. Maliyet, bant genişliği, gecikme ve yük gibi faktörlere bağlı olarak değişebilir.

Dinamik yönlendirme protokolleri, uzaklığı hesaplamak için genellikle hop mesafesini ve maliyeti birlikte kullanır. Örneğin, bir yönlendirme protokolü, bir paketin hedefe ulaşmak için geçmesi gereken en az hop sayısını ve en düşük maliyeti hesaplamak için kullanılabilir. Uzaklığın hesaplanması, dinamik yönlendirmenin verimliliğini ve güvenilirliğini önemli ölçüde etkileyebilir. Doğru uzaklık ölçümlerini kullanarak, yönlendiriciler ağdaki en iyi yolu otomatik olarak seçebilir ve paketlerin hedefe sorunsuz bir şekilde ulaşmasını sağlayabilir.

### ACCESS POİNT AP:
Kablosuz bağlantılarda kullanılan bir ağ cihazıdır. AP, kablosuz cihazların kablolu bir ağa bağlanmasına olanak tanır. Access point, kablolu bir ağ ile kablosuz bir ağ arasında bir köprü görevi görür. Access point, kablosuz cihazlardan gelen paketleri alır ve bunları kablolu ağa gönderir. Kablolu ağdan gelen paketleri de kablosuz cihazlara gönderir.

Access point'ler, farklı SSID'ler ve subnet'ler oluşturabilir. Bu, farklı kullanıcı gruplarının veya cihazların farklı ağlara bağlanmasına olanak tanır.

Örneğin, bir ofiste, çalışanlar için bir SSID ve misafirler için bir SSID oluşturulabilir. Çalışanlar SSID'si, çalışanlar için ayrılmış bir subnet'e bağlanır. Misafirler SSID'si ise, misafirler için ayrılmış bir subnet'e bağlanır.

### MODEM: MODULATOR DEMOTULATOR
__*Modulator:*__ Dijital veriyi analog veriye dönüştürür.

__*Demodulator:*__ Analog veriyi dijital veriye dönüştürür.

ADSL: Asimetrik Sayısal Abone Hattı, dijital verilerin bakır telefon hatları üzerinden iletilmesini sağlayan bir bağlantı teknolojisidir. ADSL, yüksek bant genişliği sunar, ancak uzun mesafe için performansı daha iyidir (VDSL'e göre). 

VDSL: Çoklu Hizmetli Sayısal Abone Hattı, dijital verilerin bakır telefon hatları üzerinden daha yüksek hızlarda iletilmesini sağlayan bir bağlantı teknolojisidir. VDSL, ADSL'den daha hızlıdır, ancak mesafeye bağlı olarak performansı düşer.

Ev modemleri, modulator, demodulator, access point, switch ve router gibi özellikleri bir arada toplayan cihazlardır. Ev modemleri, ev kullanıcılarının internete bağlanmasına ve diğer cihazlarla iletişim kurmasına olanak tanır.

Ev modemleri iç ağdan kendisine gelen istekleri internete yönlendirir. (Router)
Kablosuz bağlantı yayını yapar. (Access Point)
Her cihaza özel bağlantı oluşturur ve her cihazın bağlantısını bağımsız olarak yönetir. (Switch)

### Kablolar ve Kablo tipleri:
STP(Shilded Twisted Pair): Korumalı kablo olarak adlandırılır. Genelde çok fazla kablonun bulunduğu yerlerde kullanılır. Sinyal karışmasını önleyici bir koruma sağlar

UTP(Unshilded TP): Korumasız kablo. Daha ucuzdur bir koruma bulundurmaz. Sinyal karışmasına karşı dayanıklı değildir.

Fiberoptik Kablolar:
  Single Mode: Uzak mesafelere hızlı veri iletimi için kullnılan fiber optik kablo tipidir.
  Multi Mode: yakın mesafeler için kullanır. Uzak mesafelere veri iletimi sağlamaz. Ucuzdur.

### Network Topolojileri:
Bus, tüm cihazların tek bir kabloyla birbirine bağlandığı bir yapıdır. Bus topolojisi, basit ve kurulumu kolaydır. Ancak, çarpışmalara ve arızalara karşı hassastır. Çarpışmalara karşı hassastır. Ana kabloda arıza olursa, tüm ağ devre dışı kalır.

Star, her cihazın bir merkezi cihaza bağlandığı bir yapıdır. Yıldız topolojisi, çarpışmalara karşı dayanıklıdır ve arızalara karşı daha dirençlidir. Ancak, merkezi cihaz arızalanırsa, tüm ağ devre dışı kalır. Merkezi cihaz arızalanırsa, tüm ağ devre dışı kalır.

Halka, cihazların bir halka şeklinde birbirine bağlandığı bir yapıdır. Halka topolojisi, çarpışmalara karşı dayanıklıdır. Ancak, bir cihaz arızalanırsa, tüm ağ devre dışı kalır. Çarpışmalara karşı dayanıklıdır. Bir cihaz arızalanırsa, tüm ağ devre dışı kalır.

Mesh, her cihazın birbirine bağlandığı bir yapıdır. Mesh topolojisi, çarpışmalara ve arızalara karşı dayanıklıdır. Ancak, kurulumu ve yönetimi zor olabilir. En çok karşımıza çıkan yapıdır. Çarpışmalara ve arızalara karşı dayanıklıdır. Kurulumu ve yönetimi zor olabilir.

Tree, bus, yıldız veya halka topolojilerinin bir kombinasyonunu kullanan bir yapıdır. Ağaç topolojisi, karmaşık ağlar için uygundur. 

Hybrid, iki veya daha fazla topolojinin bir kombinasyonunu kullanan bir yapıdır. Hibrit topolojiler, farklı ihtiyaçları karşılamak için kullanılabilir.  

### OSI REFERANS MODELİ:
Uygulama Katmanı: google.com   HTTP HTTPS DNS FTP isteği başladı
  
Sunum Katmanı: Sıkıştırma ve şifrelemeler
 
Oturum Katmanı: oturum bilgisinin tutulduğu katman (Bütün işlemlerin ve oturumların tutulduğu yer) 
 
Taşıma Katmanı: TCP 6 ,UDP 17, 	Gelen isteğin neyle gideceği belli olur.
 
Ağ Katmanı: ICMP 1 , IP ,ARP protokolü ,AP, modem ve yönetilebilir switch
 
Veri İletim Katmanı: mac adresi burada pakete ekleniyor, 802.3 wifi  802.11 ethernet, Yönetilemez switch 
 
Fiziki Katman: Kablolar UTP STP Fiberoptik

### IP Address, OSI LAYER 3: IPV4 8 bitlik 4 oktet
Başlangıçta herkese public ip ler dağıtıldı sonrasında ip sayısı tükenmeye başlayınca private ve public ayrımı yapılmaya başlandı.
Public IP: Dış networkde kullanılacak IP
 
Private IP: İç networkde kullanılan IP

A sınıfı IP 1 ile 126 arasında tanımlanabilir. İlk oktet Ağ adresidir. Son 3 oktet host sayısını belirler. Alt ağ maskesi 255.0.0.0 şeklindedir. 10.0.0.0/8 private 

B sınıfı IP ilk iki oktet ağ adresidir. diğer iki oktet host sayısını belirler. 128 ile 191 arasında ip adresi tanımlanabilir. Alt ağ maskesi 255.255.0.0-- 172.16.0.0/12 private

C sınıfı IP İlk 3 oktet ağ adresi diğer oktet host sayısı 192 ile 223 arasında ip adresi tanımlanabilir. Alt ağ maskesi 255.255.255.0-- 192.168.0.0/16 private

D sınıfı IP 224-239 arasında ip adresi tanımlanabilir. Alt ağ maskesi yoktur multicast gruplar için saklnamıştır.

E sınıfı IP 240 ile 254 arasında ip adresi tanımlanabilir. Alt ağ maskesi yoktur araştırma için ayrılmış

**Broadcast adres**, bir ağdaki tüm cihazlara aynı anda veri göndermek için kullanılan özel bir IP adresidir. Broadcast adresleri, 255.255.255.255 olarak tanımlanır.Broadcast adresleri, ağlar arasında da kullanılabilir. Örneğin, bir yönlendirici, yayın adresini kullanarak bir sonraki yönlendiriciye bir paketi iletmesini isteyebilir. Kısaca broadcast adresleri bir ağdaki tüm cihazlara aynı anda veri göndermek için kullanılan özel IP adresleridir. Broadcast adresleri, ağlar içerisinde ve ağlar arasında kullanılabilir.
Tüm cihazların bir yanıt vermesini sağlamak için: Örneğin, bir DHCP sunucusu, yayın adresini kullanarak tüm cihazlardan IP adresi taleplerini alabilir. 

**Default Gateway Örnkele Açıklama:** Bir bilgisayarın default gateway 192.168.1.1 olarak ayarlanmıştır. Bilgisayar, 192.168.1.0/24 ağı içinde bir web sitesine erişmek istediğinde, paketi doğrudan web sitesine gönderebilir. Ancak, bilgisayar 192.168.1.0/24 ağının dışındaki bir web sitesine erişmek istediğinde, paketi varsayılan ağ geçidi 192.168.1.1'e göndermelidir. Varsayılan ağ geçidi, paketi web sitesine yönlendirir. Default gateway genelde .254 ya da .1 şeklinde tanımlanır. Arada bir ip olarak da tanımlanabilir ama bu ip'nin başka bir bilgisayardan alınmamasına dikkat edilmelidir.

### SUBNET
Subnetting, bir IP adres aralığını daha küçük aralıklara bölme işlemidir. Subnetting, bir ağdaki cihaz sayısını artırmaya, güvenlik katmanları oluşturmaya ve ağ performansını iyileştirmeye yardımcı olabilir.

192.168.3.0/24 ağı, 256 IP adresi içerir. /28 subnet maskesi, ilk 24 biti ağ adresi için ve son 4 biti alt ağ adresi için kullanır. Bu, 16 farklı alt ağ oluşturmaya izin verir.

16 farklı subnet, her biri 16 IP adresi içerir. Bu, her subnet için 15 kullanılabilir IP adresi bırakır.

Her subnet için 1 IP adresi varsayılan ağ geçidi (default gateway) olarak ayarlanır. Bu, cihazların diğer ağlara erişmesine izin verir.

Her subnet için 1 IP adresi yayın adresi (broadcast) olarak ayarlanır. Bu, bir subnetteki tüm cihazlara bir mesaj göndermek için kullanılır.

Özetle, 192.168.3.0/24 ağını /28 subnet maskesi kullanarak 16 farklı subnete nasıl böleceğimizi anlatmaktadır.

Örnek:

192.168.3.0/24 ağındaki ilk subnet, 192.168.3.0/30'dur. Bu, ilk 24 biti ağ adresi için ve son 2 biti alt ağ adresi için kullanır. Bu subnet, 192.168.3.0 ile 192.168.3.1 arasındaki 2 IP adresini içerir.

Bu subnet için varsayılan ağ geçidi 192.168.3.1'dir. Bu subnet için yayın adresi 192.168.3.255'tir.

Diğer subnetler de benzer şekilde ayarlanır.

### VLAN:
VLAN, bir yerel alan ağında (LAN) bulunan cihazları mantıksal olarak gruplandırmak için kullanılan bir yöntemdir. VLAN'lar, güvenlik, ölçeklenebilirlik, kontrol ve performans gibi çeşitli avantajlar sunar.

VLAN'ların avantajları:

__*Güvenlik:*__ VLAN'lar, bir ağdaki cihazları fiziksel konumuna göre değil, işlevselliğine göre gruplandırarak güvenlik katmanları oluşturabilir. Örneğin, bir ofiste, çalışanlar ve ziyaretçiler farklı VLAN'larda gruplandırılabilir. Bu, çalışanların verilerinin ziyaretçiler tarafından erişilmesini engellemeye yardımcı olur. Farklı vlanlar için farklı kurallar yazılabilir.
__*Ölçeklenebilirlik:*__ VLAN'lar, bir ağın ölçeklenebilirliğini artırabilir. Örneğin, bir ağın fiziksel boyutu büyüdükçe, VLAN'lar, ağ trafiğini tek bir noktadan yönetmeyi kolaylaştırabilir.
Kontrol: VLAN'lar, bir ağdaki cihazların erişimini kontrol edebilir. Örneğin, bir ofiste, çalışanlar ve ziyaretçiler farklı VLAN'larda gruplandırılabilir. Bu, çalışanların yalnızca kendi VLAN'larında bulunan kaynaklara erişmesine izin verir.
__*Performans:*__ VLAN'lar, bir ağdaki performansı iyileştirebilir. Örneğin, bir ağda, ses ve video gibi farklı türde trafik için ayrı VLAN'lar oluşturulabilir. Bu, farklı türdeki trafiklerin birbirini etkilemesini engellemeye yardımcı olur.

Trunk
Access
Default

**VTP:** VTP, birden fazla anahtarın bulunduğu ağlarda VLAN'ları yönetmek için kullanılan bir protokoldür. VTP, anahtarların VLAN bilgilerini birbirleriyle paylaşmasını sağlar. Bu, VLAN'ları tek bir yerden yönetmeyi kolaylaştırır.

VTP'nin avantajları:

Tek bir yerden yönetim: VTP, VLAN'ları tek bir yerden yönetmeyi kolaylaştırır. Bu, ağ yöneticilerinin zaman ve çabadan tasarruf etmesine yardımcı olur.
Daha az hata: VTP, VLAN bilgilerinin otomatik olarak paylaşılmasını sağlar. Bu, VLAN bilgilerinin yanlışlıkla değiştirilmesini veya kaybolmasını engellemeye yardımcı olur.
Daha fazla güvenlik: VTP, VLAN bilgilerinin yetkisiz erişime karşı korunmasına yardımcı olur.

VTP Domain: VTP domain, aynı VTP protokolünü kullanan anahtarların oluşturduğu bir gruptur. Bir VTP domain'de, anahtarlar VLAN bilgilerini birbirleriyle paylaşır.

### Firewall:

Ağ Güvenlik Duvarı (Firewall), bir ağdaki cihazları yetkisiz erişime ve saldırılara karşı korumak için kullanılan bir güvenlik cihazıdır. IPS IDS görevi görür. Ağ güvenlik duvarları, gelen ve giden ağ trafiğini analiz ederek, izin verilen trafiği içeri alır ve izin verilmeyen trafiği engeller. Kendi loglarını üzerinde de tutabilir farklı bir cihazda da tutabilir. Ayrıca IP reputation ve antibot sağlar. IP reputation, bir IP adresinin geçmişteki davranışlarına dayanarak güvenilirliğini tahmin etmek için kullanılan bir tekniktir. Antibot, kötü amaçlı yazılım içeren web sitelerine ve kaynaklara erişimi engellemek için kullanılan bir tekniktir.

Güvenlik, Yönetilebilirlik, Ölçeklendirme, Politikalandırma ve Zafiyet Önlemi sağlar

VPN: SSL VPN, bir cihazın bir VPN sunucusu aracılığıyla bir ağdaki diğer cihazlara güvenli bir şekilde bağlanmasına olanak tanıyan bir VPN protokolüdür. SSL VPN, güvenli soket katmanı (SSL) protokolünü kullanır ve genellikle web tarayıcıları aracılığıyla kullanılır.
IPSEC, bir cihazın bir VPN sunucusu aracılığıyla bir ağdaki diğer cihazlara güvenli bir şekilde bağlanmasına olanak tanıyan bir VPN protokolüdür. IPSEC, IPSec protokolünü kullanır ve genellikle ağ geçitleri veya özel yazılım aracılığıyla kullanılır.
SSL VPN'nin portu 10443'tür. Bu port, SSL VPN bağlantılarını kabul etmek için kullanılır.

SSL VPN, yerel bir cihazda, bir etki alanı denetleyicisinde veya bir RADIUS sunucusunda kullanılabilir.

IPSEC yapılandırma ağ public ve static olmalıdır. Bu, IPSEC bağlantısının her iki ucundaki cihazların da birbirleriyle iletişim kurabilmesi için bir halka ağda olması gerektiği anlamına gelir. Ayrıca, her iki ucundaki cihazların da statik IP adresleri olması gerekir.

IPSEC bağlantısının her iki ucundaki şifreleme ve kimlik doğrulama yöntemleri de aynı olmalıdır. Bu, bağlantının güvenli ve güvenilir olmasını sağlamak için önemlidir.

**Firewall Kullanım Amaçları:**

__*UTM koruması:*__ UTM koruması, bir güvenlik duvarının bir dizi güvenlik özelliğini sağlamasıdır. Bu özellikler, URL filtreleme, uygulama denetimi, IPS ve diğer güvenlik önlemlerini içerebilir. Firewall üzerinde UTP profilleri oluştururuz. Bu oluşturduğumuz profillere göre kurallar yazabilme imkanına sahip oluruz.

__*QOS:*__ QOS, bir ağda belirli paketlere öncelik verilmesine olanak tanıyan bir tekniktir. Bu, ağ performansını iyileştirmek veya belirli uygulamalara veya hizmetlere öncelik vermek için kullanılabilir.

__*SD-WAN:*__ SD-WAN, bir kuruluşun birden fazla geniş alan ağ (WAN) bağlantısını yönetmesine olanak tanıyan bir teknolojidir. SD-WAN, hat yedeklemesi, kesintisiz erişim ve SLA yönetimi gibi özellikleri sağlayabilir. Uzak konumlarda farklı IPSEC bağlantıları kurmak için kullanılabilir.

__*NAT:*__ Public IP'ler artık yetersiz gelmeye başladı. Nat bir cihazın yerel ağındaki özel IP adreslerini, bir halka ağdaki genel IP adreslerine dönüştüren bir tekniktir. Bu, bir kuruluşun birden fazla cihazı tek bir halka IP adresine sahip bir İnternet bağlantısı aracılığıyla dışarıya bağlamasına olanak tanır.

NAT, yerel ağınızın tüm cihazlarının tek bir public IP adresini kullanmasına olanak tanır.
Aynı zamanda birden fazla cihaz başka bir ağa tek bir ip den çıkış yapabilir. Bu, NAT'ın bir başka özelliğidir. NAT, bir cihazın IP adresini değiştirerek, birden fazla cihazın aynı IP adresini kullanarak aynı ağa bağlanmasına olanak tanır.

Örnek:

Şirketin yerel ağında 100 cihaz vardır. Bu cihazların tümü 10.0.0.0 ile 10.255.255.255 arasındaki IP adreslerini kullanır. Şirket, bu cihazların hepsinin İnternet'e erişmesini istiyor.

Şirket, NAT'ı kullanarak bu sorunu çözebilir. NAT, yerel ağın tüm cihazlarının tek bir halka açık IP adresini kullanmasına olanak tanır. Bu durumda, halka IP adresi 10.0.0.1 olabilir.

Şirket, NAT'ı kullanarak aynı zamanda birden fazla cihazın aynı ağa bağlanmasına da olanak tanıyabilir. Örneğin, şirket, bir web sunucusunun 10.0.0.10 IP adresini kullanmasını ister. Şirket, NAT'ı kullanarak bu web sunucusunun IP adresini 10.0.0.1'e değiştirebilir. Bu, web sunucusunun başka bir ağa bağlanan diğer cihazlarla aynı IP adresini kullanmasına olanak tanır.

