# Git Notları 

Git bir versiyon kontrol sistemidir.

## GİT TERMİNAL KULLANIMI 
```bash 

ls        # içinde olduğun dizindeki klasörleri ve dosyaları listeler
pwd       # içinde olduğun dizini verir
cd        # dizin değiştirir 
cd ..     # bir önceki dizine gelir 
mkdir     # yeni klasör oluşturur 
touch     # dosya oluşturur
rm        # dosyayı siler
rm -rf    # klasörü siler
clear     # terminali temizler
```

### Örnek
```bash
mkdir not     # not diye bir klasör oluşturur
cd not/        # not klasörünün içine girer
touch x.txt    # x adında bir txt dosyası oluşturur 
rm x.txt       # x.txt dosyasını siler 
cd ..          # not klasöründen çıkar 
rm -rf not     # not klasörünü siler
``` 

##  Git Komutları
```bash
git status                 # git init kullanmadan önce kullanılmalıdır, güncel git durumunu gösterir
git init                   # git başlatır
git add "ornek.py"         # ornek.py dosyasını git'e ekler
git add .                  # projedeki tüm dosyaları git'e ekler
git commit                 # projede yapılan değişiklikleri belirtmek için kullanılır
git commit -m "message"    # message commitini atar
git commit -a -m "message" # git'e eklenmiş dosyaları otomatik commit eder
git log                    # commit geçmişini listeler 
.gitignore                 # GitHub'a yüklenmesini istemediğimiz dosyaları belirtmek için kullanılır 
```

- Örnek: Bir gizli.txt dosyamız olsun ve içinde API key bulunduruyor ama bu API key gizli kalmalı.Bu dosyayı .gitignore dosyasının içine yazarsak projeyi GitHub'a attığımızda gizli.txt dosyası gözükmez yani API key gizli kalmış olur.

## Git Branch 

Branch , Git'in temel parçasıdır ve kod tabanındaki değişikleri yönetmek için kullanılır. Mesela bir proje üzerinde çalışırken farklı branch'ler açarak izole ortamlar yaratabiliriz.Her branch farklı bir işlevi temsil eder, bu sayede farklı geliştiriciler aynı anda bağımsız olarak çalışabilir.

HEAD -> projede  mevcut dalı (branch) gösteren bir işaretçidir (pointer)

## Branch Komutları
```bash
git branch                    # mevcut branch'leri listeler
git branch branch_ismi        # yeni branch oluşturur 
git branch feature            # feature adında branch oluşturur 
git switch branch_ismi        # mevcut daldan (branch) başka bir dala geçmeyi sağlar 
git switch feature            # artık feature dalında devam eder 
```

## Merge 
```bash
git merge branch_ismi         # dalları birleştirir
```

-Örnek: Mesela projenin başında ana branch main sonra yeni branch olarak feature oluşturduk.Bu iki dalı birleştirmek için main dalına geri döneriz ve feature ile birleştiririz.
```bash
git switch main
git merge feature 
```

## Git Stash 
```bash
git stash           # gizlenmesini istediğimiz şeyleri stash içine alırız
git stash list      # stash içindekileri listeler
git stash pop       # stash içindekini geri getirir 
git stash apply     # geri uygular 
git stash clear     # stash içini temizler artık gizli bir şey kalmaz
```

## Geçmişe Dönme 
```bash
git restore ornek.txt # diyelim ki ornek.txt dosyasına bir şeyler yazılmış ve commit edilmiş sonradan üzerinde değişiklik yapılmış ve kaydedilmiş ama commit edilmemiş bir önceki committeki haline gitmek istiyorsak restore ile bu işlemi yaparız 

git checkout commit_id # belirtilen commite döneriz, head o commiti gösterir sonraki commitler silinmez yani sadece o an o commitle çalışırız

git reset commit_id # belirtilen commite döneriz, head o commiti gösterir ondan sonraki commitler silinir ama dosya içeriği aynı kalır

git reset --hard commit_id  # belirtilen commite döneriz, head o commiti gösterir ondan sonraki commitler ve yapılan tüm değişiklikler silinir  

git revert commit_id  # belirtilen committe yapılan değişiklikleri geri alır, head en son committe kalır ve silme işlemi yapmadan bu değişikliği geri alan yeni bir commit ekler
```

## Karşılaştırma 
```bash
git diff               # branchler, dosyalar veya head'ler arasındaki farkları gösterir
git diff main feature  # main ve feature branchleri arasındaki farkları gösterir
```

## Rebase 
```bash
git rebase             # git'in bir dalındaki değişiklikleri başka bir dala entegre eder  
```
Örnek : feature dalının içindeyken git rebase main dersek feature dalındaki değişiklikler main dalının ucuna sıralanır ve düzenli bir görünüm oluşur 
```bash
git switch feature 
git rebase main 
```   




