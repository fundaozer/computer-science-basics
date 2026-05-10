# Dosya Sistemleri ve Depolama Mantğı

## NTFS – ext4 – APFS Farkları

### NTFS (New Technology File System):
Windows işletim sisteminin kullandığı dosya sistemidir. Güvenlik, izin yönetimi ve büyük dosya desteği sunar.

### ext4 (Fourth Extended File System):
Linux sistemlerinde yaygın olarak kullanılır. Hızlı, kararlı ve düşük kaynak tüketimine sahiptir.

### APFS (Apple File System):
Apple’ın macOS ve iOS cihazları için geliştirdiği modern dosya sistemidir. SSD’ler için optimize edilmiştir ve şifreleme desteği güçlüdür.

## Blok Yapısı Nedir?

Depolama aygıtlarında veriler tek parça halinde tutulmaz. Küçük parçalara ayrılarak saklanır, bu parçalara blok (block) denir.

Örneğin bir dosya kaydedildiğinde:

-Dosya küçük veri bloklarına bölünür.
-Disk üzerinde uygun yerlere yazılır.
-İşletim sistemi bu blokların yerini takip eder.

Bu yapı sayesinde:

-Veri daha düzenli saklanır.
-Okuma/yazma işlemleri hızlanır.
-Disk yönetimi kolaylaşır.


## HDD vs SSD Çalışma Prensipleri

### HDD (Hard Disk Drive)

HDD, dönen manyetik diskler kullanarak çalışır.
Veri okumak için mekanik bir kafa fiziksel olarak hareket eder.

Özellikleri:

-Daha ucuzdur.
-Daha yüksek kapasite sunabilir.
-Mekanik olduğu için daha yavaştır.
-Darbelere karşı hassastır.

### SSD (Solid State Drive)

SSD, verileri flash bellek üzerinde elektronik olarak saklar. Hareketli parça içermez.

Özellikleri:

-Çok daha hızlıdır.
-Sessiz çalışır.
-Daha dayanıklıdır.
-Açılış ve program yükleme süreleri kısadır.