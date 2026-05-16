# Linux Temelleri

## Terminal Komutları

Linux sistemlerinde işlemlerin büyük kısmı terminal üzerinden yapılır. En sık kullanılan temel komutlardan bazıları şunlardır:

- **ls:** Bulunulan klasördeki dosya ve klasörleri listeler.  
- **cd:** Klasörler arasında geçiş yapmayı sağlar.  
- **grep:** Dosya içinde belirli bir metni arar.  
- **mkdir:** Yeni klasör oluşturur.  
- **chmod:** Dosya ve klasör izinlerini değiştirir.  
- **top:** Sistemde çalışan işlemleri ve kaynak kullanımını gösterir.  

---

## Paket Yönetimi (apt / pacman / dnf)

Linux dağıtımlarında program yüklemek, güncellemek ve kaldırmak için paket yöneticileri kullanılır.

- **apt:** Debian ve Ubuntu tabanlı sistemlerde kullanılır.  
- **pacman:** Arch Linux tabanlı sistemlerde kullanılır.  
- **dnf:** Fedora ve Red Hat tabanlı sistemlerde kullanılır.  

Örneğin bir program yüklemek için:

```bash
sudo apt install program_adi
```

---

## Dosya İzinleri

Linux’ta her dosya ve klasör için kullanıcı izinleri bulunur.

Temel izinler:
- **r (read):** Okuma izni  
- **w (write):** Yazma izni  
- **x (execute):** Çalıştırma izni  

Bu izinler sayesinde sistem güvenliği sağlanır ve kullanıcıların erişimleri kontrol edilir.

---

## Servisler (systemctl)

Linux’ta arka planda çalışan servisler `systemctl` komutu ile yönetilir.

Sık kullanılan örnekler:

```bash
systemctl status servis_adi
```

Servisin durumunu gösterir.

```bash
systemctl start servis_adi
```

Servisi başlatır.

```bash
systemctl stop servis_adi
```

Servisi durdurur.

---

