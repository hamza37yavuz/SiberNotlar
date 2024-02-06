# Active Directory

## Active Directory Mantıksal Yapı Bileşenleri
**FOREST:** AD'nin domainlerinden mantıksal yapıdaki en dış katmandırç İçerisinde bir ya da birden fazla domain barındıran yapıya forest denir. Forest içinde kurulan ilk domaine Forest Root Domain adı verilir. Aynı forest içinde farklı isimlerde domainler olabilir.

**DOMAIN TREE:** Aynı isim altında toplanmış bir veya birden fazla sayıda domainin hiyerarşik olarak oluşturduğu yapıya verilen isimdir.

**DOMAIN:** Kullanıcıların ve bilgisayar, yazıcılar gibi kynakların bir arada aynı ağ içerisinde hiyerarşik şekilde çalışmasını sağlayan yapılardır.

## Active Directory Fiziksel Yapı Bileşenleri
**SITE:** Domain yapısında DC'ler arası replikasyon ve bağlantı trafiğini kontrol altına almak için oluşturulan yapılardır.

**DOMAIN CONTROLLER:** Domain yapısını kuran ve domain içerisindeki bütün objelerin ve kaynakların veri tabanını depolayan bilgisayarlara DC (Domain Controller) adı verilir. Kimlik doğrulama isteklerine yanıt veren ve bilgisayar ağlarındaki kullanıcıları doğrulayan bir sunucudur. Tüm verilerin düzenli ve güvenli olarak tutulduğu sunucudur.

## Domain Controller Seçenekleri
**ROOT DC:** bir domain tree içerisinde en tepede olan ve ilk kurulan domaine root domain denir. O domainin domain controller sunucusna root domain controller denir.

**PRIMARY DC:** AD kurulumu yapılan ilk server bilgisayar Primary Domain Controller olarak görev alır. Bir domain ortamında yalnızca bir tane olur.

**ADDITIONAL DC:** Yedeklilik sağlamak ve performansı arttırmak noktasında yapılandırılan ikincil sunuculara Additional DC adı verilir.

**READ ONLY DC:** AD hizmetlerini sadece salt okunur olarak sunan DC sunuculara verilen isimdir. Güvenlik amacıyla kullanılan yapıdır.

**Organizational Unit Nedir:** Domain içerisindeki kullanıcıları grupları veya bilgisayarları organize etmek için oluşturulmuş nesnelerdir. AD nesnelerini hiyerarşişk olarak gruplamak için kullanılır.

## FSMO Rolleri Nelerdir:
Açılımı Flexible Single Master Operation dur. AD yapısındaki 5 temel rolü temsil eder. AD mimarisinde PDC Emulator, RID Master, Schema Master, Domain Naming Master ve Infrastructure Master olmak üzere 5 rol bulunmaktadır.

**Forest FSMO Rolleri:** Schema Master, Domain Naming Master

**SCHEMA MASTER:** AD şemasının yönetilmesinden ve tüm forest çapındaki domainlerin DC'lerine replikasyonun yapılmasından sorumludur. Her forestta sadece bir tane bulunur.

**DOMAIN NAMING MASTER:** Forest içinde yeni domain ya da domain tree oluşturulmasını veya silinmesini denetler. Oluşturulmak istenen yeni domainlerin tüm forestte tek olduğunu kontrol eder. Her forestte sadece bir tane bulunur.

**Domain FSMO Rolleri:** RID Master, PDC Emulator, Infrastructure Master

**RID MASTER:** AD üzerinde oluşturulacak nesnelerin Security Identifier SID numaralarının üretilmesinde kullanılacak RID'lerin üretilip DC lere gönderilmesinden sorumludur. Her bir etki alanında sadece bir adet RID Master rolü üstlenen DC bulunabilir.

**PDC EMULATOR:** Senkronize zaman ile çalışmasını sağlar. Kayıt bilgileri group policy ve sysvol erişimlerini yönetir.

**INFRASTURCTURE MASTER:** Tek görevi kendi domainimizdeki bir nesnenin başka bir domaindeki gruba eklenmesi durumunda ilgili nesnenin güncellemelerinin diğer etki alanına yapılmasından sorumludur.

## DNS Kayıtları Nelerdir:
**A KAYDI:** Address kaydı en temel kayıt türüdür. İsimleri IP'ler ile eşler

**CNAME:** Bir host için takma ad alias oluşturma amacıyla kullanılır.

**MX:** Alan adına gelen e-postaların yönlendirileceği mail sunucu bilgilerini içerir.

**PTR:** E-posta hizmetlerinin sağlıklı çalışması için önemlidri. A kayıtlarının tam tersi mantıkta çalışır. IP'de isme eşleme yapar.(MAİL GÜVENLİK DOĞRULAMA)

**TXT:** Özel amaçlar için oluşturulan bir kayıt türüdür. Bir host için birden fazla TXT kaydı bulunabilir.SPF DKIM MARC yaygın olarak kullanılan txt kayıtlarıdır.

**SOA:** Yetki bölgesi anlamına gelir DNS kuruluşlarıyla ilgili bilgileri içerir. Bu yüzden her domainin SOA kaydı bulunmaktadır.

# SANALLAŞTIRMA
## Sunucu Sanallaştırma Sistemi Bileşenleri:
__*Hypervisor:*__ Fiziksel Donanım üzerinde çalışarak sanal makinenin oluşturulmasını ve yönetilmesini sağlayan yazılımdır.

__*Sanal Makineler:*__ Her biri bağımsız işletim sistemini ve uygulamaları barındıran sanal sunuculardır. İzolasyon ve bağımsızlık sağlar.

__*Sanallaştırılmış Kaynaklar:*__ Sanal makinelerin kullanımına sunulan işlemci bellek depolama ve ağ kaynaklarının sanallaştırılmasıdır.

__*Template ve Snapshotlar*__     __*Storage*__     __*Networking*__

## Sanallaştırmada Cluster Yapısı Nedir:
Birden çok fiziksel sunucun bir araya getirilerek tek bir mantıksal birim olarak çalışmasını sağlayan bir yapıdır. Yüksek erişilebilirlik performans iş yüklerinin otomatik yönetilmsei gibi avantajlar sağlar. Genellikle bir hypervisor kullanılarak makinelerin veya konteynırların bu fiziksel sunucu üzerinde dağıtılmasına olanak tanır.

Nelerden Oluşur: Fiziksel Sunucular, Hypervisor, Yük Dengeleme (Load Balancer), Yedekleme, Yüksek Erişilebilirlik (HA), Ortak Depolama, Yönetim ve İzleme Aracı  

## Hyper Converged Mimari Nedir:
Bu yapı HCI bir organizasyonun bilişim kaynaklarını entegre etmek ve birleştirmek amacıyla kullanılan bir mimaridir. Depolama, hesaplama, ağ ve yönetim işlevlerini tek bir entegre sistemde birleştirir. Bu yaoı sayesinde esneklik ve performans artışı kazanılır. Merkezi bir noktadan yönetilebilir.
