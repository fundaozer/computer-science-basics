# İşletim Sistemi Temelleri (OS Basics)

## Kernel (Çekirdek)

Kernel, bir işletim sisteminin temel parçasıdır; donanım ile yazılım arasındaki iletişimi yöneten , sistem kaynaklarını (CPU, bellek,depolama, aygıtlar) kontrol eden en alt seviye yazılım köprüsüdür. Sistem açılışında yüklenir ve kapanana kadar çalışır. Uygulamaların donanıma güvenli erişmesini sağlar ve sistem kararlılığını korur.
## Süreç (Process) - İş Parçacığı (Thread) Farkı

Bellek Paylaşımı: Process'ler birbirinden bağımsız adres alanlarına sahiptir. Thread'ler ise aynı process'in bellek alanını paylaşır.

Bağımsızlık: Bir process çökerse diğerlerini etkilemez. Ancak bir thread çökerse, bağlı olduğu process'i de etkileyebilir.

Maliyet: Process oluşturma ve geçiş (context switch) maliyeti yüksektir. Thread oluşturma ve geçiş çok daha hızlı ve maliyeti düşüktür.

İletişim: Process'ler arası iletişim  karmaşıktır. Thread'ler arası iletişim, aynı hafızayı paylaştıkları için daha kolaydır.

Yapı: Process, işletim sistemi kaynaklarını (dosyalar, bellek) yönetir. Thread ise doğrudan CPU'da çalıştırılacak görevleri (kod) yürütür. 

## Bellek Yönetimi

Bellek yönetimi, işletim sisteminin RAM’i programlara verimli şekilde dağıtması ve yönetmesidir. Amaç; performansı artırmak ve bellek hatalarını önlemektir.

Temel yöntemler:

-Dinamik bellek yönetimi (Heap/Stack): Programlar ihtiyaç duydukça bellek alır (malloc, new) ve işi bitince geri bırakır (free, delete).
-Çöp toplama (Garbage Collector): Java ve Python gibi dillerde, kullanılmayan veriler otomatik silinir.
-Sanal bellek (Virtual Memory): RAM yetmezse, disk geçici olarak RAM gibi kullanılır.
-Sayfalama (Paging): Bellek küçük sabit parçalara bölünerek daha verimli kullanılır.
-Bölütleme (Segmentation): Bellek, kod ve veri gibi mantıksal bölümlere ayrılır.

## CPU Zamanlayıcıları 

CPU zamanlayıcıları, işletim sisteminde birden fazla süreç arasından hangisinin ne zaman çalışacağını belirleyen mekanizmalardır. Amaç, işlemciyi verimli kullanmak ve bekleme sürelerini azaltmaktır.

Temel algoritmalar:

-FCFS (First Come First Serve): İlk gelen süreç önce çalışır.
-SJF (Shortest Job First): En kısa süren iş önce çalışır.
-Round Robin: Her sürece eşit süre verilir, sırayla döner.
-Priority Scheduling: Önceliği yüksek olan süreçler önce çalışır.