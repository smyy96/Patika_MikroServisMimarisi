# Mikroservis Mimarisi

### Monolitik Mimari (Monolithic Architecture)
```
  Client'larımız sunucuya istek gönderiyor ve bu istek doğrultusunda sunucu ise o 
  isteğe bağlı olarak databaseden verileri çekip kullanıcıya sunuyor. Sürekli olarak 
  kullandığımız bir mimari türüdür. Bu mimariye monolitik mimari denir.  
  
  Monolitik mimaride sunucu içerisinde 3 tane katman vardır.
  ○ User Interface : Kullanıcının(client'ın) gördüğü bölüm.
  ○ Business Layer: Mantıksal işlemlerin yapıldığı yer yani kodların yazıldıgı bölüm.
  ○ Data Access Layer: Veritabanına bağlandığımız ve veri istediğimiz bölüm.
  
  Monolitik Mimari Ölçeklendirme
  Kullanıcılar yoğun istek attıklarında database, sorgulara yetişememeye başlıyor ayriyeten 
  sunucunun kaynaklarıda yetersiz kalabiliyor. Bu durumdan kurtulmak için sunucuyu
  ölçeklendiriyoruz yani kopyasını alıyoruz ve diğer sunuculara aktarıyoruz. Peki gelen 
  istekleri bu sunucular arasında hangisine yönlendireceğimize nasıl karar veriyoruz dersek bunu 
  load balancer ile yapıyoruz. Load Balancer, client üzerinden gelen istekleri duruma göre sunucular
  üzerinde paylaştırır.
  
  Monolitik Mimari Avantajları
  * Geliştirmesi basit,
  * Test edilebilirliği kolay,
  * Deployment kolay,
  * Ölçeklendirme kolay
  
  Monolitik Mimari Dezavantajları
  * Bakımı proje büyüdükçe zor,
  * Uygulamanın boyutu başlama süresini yavaşlatır,
  * Ölçeklendirileceği zaman sorun çıkartabilir,
  * Ölçeklendirme tüm proje genelinde yapılır yani sadece yoğunluk olan bölümü ölçeklendiremiyoruz,
  * Güvenilirlik/Sağlamlık/Dayanıklılık
  
```

![image](https://user-images.githubusercontent.com/62007900/186894883-07d0091f-dd6d-4ff9-ab47-f72d202e38ad.png)
<img src="https://user-images.githubusercontent.com/62007900/186898203-792ab1b5-d47b-4373-b48b-720c5549b788.png" width="350" height="235">


### SOA (Service Oriented Architecture)
```
  Servislerin ayrı ayrı tasarlanıp, bir yapı oluşturmasını sağlar.
  Yapılar birbirlerinden bağımsız olarak çalışabilirler. (loose coupling)
  Birden çok sistemin yer aldığı yapılarda kullanılır.
  Kendi içerisinde bir çok bileşeni vardır.
    ○ Policies, Contractsi Services ve çok daha fazlası
  Dağıtık yazılım sistemlerinin kalitelerini arttırmayı hedefler.
    ○ Tekrar kullanılabilirlik
    ○ Uyumluluk
    ○ Bakım Yeteneği
    
  
   SOA Avantajları
  * Servisler tekrar kullanılabilir,
  * Servislerin bakım ve onarım süreçleri kolaydır,
  * Güvenirlilik/Dayanıklılık,
  * Yatay ve dikey ölçeklendirme mümkündür,
  * Platform bağımsızdır,
  * Üretkenlik arttar
  
  SOA Dezavantajları
  * Overload,
  * Yüksek bant genişliği,
  * Yüksek maliyet
 
```

### Mikroservisler Mimarisi (Service Oriented Architecture)
```
  * SOA'nın bir yorumudur.
  * Her bir servisin kendine ait bir dünyada çalışmasını hedefler. 
      Yani her bir servis kendine ait sunucuda çalışacak.
  * Her bir servisin kendine ait veritabanı vardır.
  * Sadece bir küçük işi çok iyi yapmalıdır. 
  * Kendi aralarında ise Api Gateway üzerinden iletişime geçerler.
  * Stateless yapılardır.
  * Kolay Ölçeklenebilirler. (Yatay) 
  
  
  Mikroservis Avantajları
  * Çok dilli mimari,
  * Kolay ölçeklendirme,
  * Daha iyi bir takım yönetimi,
  * Yenilik yapmak daha kolay,
  * Mikroservislerin kendine ait veritabanı vardır,
  * Implemente edilirken diğer servisler etkilenmez.
  
  Mikroservis Dezavantajları
  * Implementasyon kolay değildir,
  * Debug kolay değildir,
  * Hata yönetimi kolay değildir.
  
```
<img src="https://media-exp1.licdn.com/dms/image/C4D12AQHm9xJ4AaXGDQ/article-inline_image-shrink_1000_1488/0/1603974909794?e=1666828800&v=beta&t=5oyWvacKJO6jdJax583Q76zYHSP0CJ5rqnCgUfYigPY" width="425" height="235">










