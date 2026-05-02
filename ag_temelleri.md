# Ağ Temelleri (Networking)

## IP, Port, DNS, TCP, UDP Nedir?

-IP (Internet Protocol):İnternetteki cihazların kimliğidir. Her cihazın bir IP adresi vardır ve bu sayede birbirlerini bulurlar.

-Port:Aynı cihaz içinde hangi uygulamaya gidileceğini belirler.
Örneğin bir bilgisayarda hem web sitesi hem de başka servisler aynı anda çalışabilir, port bunları ayırır.

-DNS (Domain Name System):İnsanların hatırlaması kolay olan alan adlarını (örneğin google.com), IP adreslerine çevirir.

-TCP (Transmission Control Protocol):Güvenilir veri iletimi sağlar. Veri kaybolursa tekrar gönderir, sıralamayı korur.
(Daha yavaş ama güvenli)

-UDP (User Datagram Protocol):Daha hızlıdır ama veri kaybı kontrolü yoktur.Genelde video, oyun gibi hızın önemli olduğu yerlerde kullanılır.

## Paket Yapısı Nasıl Çalışır?

İnternette veri tek parça halinde gönderilmez. Küçük parçalara bölünür, bunlara paket (packet) denir.

Her paket:

-Gönderici adresi (IP)
-Alıcı adresi (IP)
-Veri (payload)

bilgilerini içerir.

Bu paketler ağ üzerinden ayrı ayrı gider ve hedefte tekrar birleştirilir.Yani aslında bir mesaj gönderdiğinde, o mesaj parçalanıp farklı yollardan bile gidebilir.

## Ping, Traceroute, Nslookup Ne İşe Yarar?

-Ping:Bir sunucuya ulaşılıp ulaşılamadığını test eder.Aynı zamanda gecikme süresini (latency) gösterir.

-Traceroute (tracert):Verinin hedefe giderken geçtiği yolları (router’ları) gösterir.Nerede yavaşlama olduğunu anlamak için kullanılır.

-Nslookup:Bir domain’in hangi IP adresine karşılık geldiğini öğrenmek için kullanılır.