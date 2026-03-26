# Git Notları 

Git bir versiyon kontrol sistemidir.

## GİT TERMİNAL KULLANIMI 

ls        # içinde olduğun dizindeki klasörleri dosyaları listeler
pwd       # içinde olduğun dizini verir
cd        # dizin değiştirir 
cd ..     # bir önceki dizine gelir 
mkdir     # içinde olduğun dizinde yeni klasör oluşturur 
touch     # dosya oluşturur
rm        # dosyayı siler
rm -rf    # klasörü siler
clear     # terminalde yazılanları siler

örnek : mkdir not = not diye bir klasör oluşturdu
        cd not/ = not klasörünün içine girer
        touch x.txt = x adında bir txt dosyası oluşturur 
        rm x.txt = x.txt dosyasını siler 
        cd .. = not klasöründen çıkar 
        rm -rf not = not klasörünü siler 

## Komutlar 

git status # git init kullanmadan önce kullanılmalıdır, güncel git durumunu gösterir

git init # git başlatır

git add "ornek.py" # ornek.py dosyasını git'e ekler

git add . # projedeki tüm dosyaları git'e ekler

git commit # projede yapılan değişiklikleri belirtmek için kullanılır

git commit -m "message" # message commitini atar

git commit -a -m "message" # git'e tanıtılmış tüm dosyalardaki değişiklikler önce add yapılır sonra commit edilir

git log # projenin tüm commit geçmişini listeler 

.gitignore # bu dosyanın içine kodlarımızı githuba veya başka bir platforma attığımızda başka insanlara görünmesini istemediğimiz dosyaları koyarız mesela bir gizli.txt dosyası içinde apı key bulunduruyorsak .gitignore dosyasının içine gizli.txt yazarız ki apı key gizli kalsın 

## Git Branch 

Branch , Git'in temel parçasıdır ve kod tabanındaki değişikleri yönetmek için kullanılır. Mesela bir proje üzerinde çalışırken farklı branch'ler açarak izole ortamlar yaratabiliriz.Her branch farklı bir işlevi temsil eder, bU sayede farklı geliştiriciler aynı anda bağımsız olarak çalışabilir.

head  # projede  mevcut dalı (branch) gösteren bir işaretçidir (pointer)
merge  # projede dalları (branch) birleştiren yapı

Terminalde

git branch # mevcut branch'leri listeler

git branch branch_ismi  # yeni branch oluşturur 
Örnek:   git branch feature  # feature adında branch oluşturur 

git switch branch_ismi # mevcut daldan (branch) başka bir dala geçmeyi sağlar 
Örnek:  git switch feature  # artık feature dalında devam eder 

git merge branch_ismi  # dalları birleştirir
Örnek:   diyelim ki projenin başında ana branch main sonra yeni branch olarak feature oluşturduk.Bu iki dalı birleştirmek için main dalına geri döneriz ve feature ile birleştiririz
      -  git switch main
      -  git merge feature 



