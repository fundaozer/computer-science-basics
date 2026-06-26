# Yazılım Mimarisi Temelleri

## Monolith vs Microservice

Yazılım mimarisi, bir uygulamanın nasıl yapılandırıldığını ve bileşenlerinin nasıl iletişim kurduğunu belirler. En yaygın iki yaklaşım Monolith ve Microservice mimarileridir.

### Monolith Mimarisi

Monolith mimarisinde uygulamanın tüm bileşenleri tek bir proje ve tek bir uygulama olarak geliştirilir ve dağıtılır.

Özellikleri:
- Geliştirmesi ve kurulumu daha kolaydır.
- Küçük ve orta ölçekli projeler için uygundur.
- Tüm sistem tek parça halinde çalışır.
- Bir bölümdeki hata tüm sistemi etkileyebilir.

Örnek:

```text
Kullanıcı Yönetimi
Ürün Yönetimi
Sipariş Yönetimi
↓
Tek Uygulama
```

---

### Microservice Mimarisi

Microservice mimarisinde uygulama, bağımsız servislerden oluşur. Her servis belirli bir görevi yerine getirir ve diğer servislerle API üzerinden iletişim kurar.

Özellikleri:
- Her servis bağımsız olarak geliştirilebilir.
- Büyük ölçekli sistemler için uygundur.
- Ölçeklendirme daha kolaydır.
- Yönetimi ve dağıtımı daha karmaşıktır.

Örnek:

```text
Kullanıcı Servisi
Ürün Servisi
Sipariş Servisi
Ödeme Servisi

↓ API İletişimi ↓
```

---

## MVC ve MVVM Mimari Desenleri

Mimari desenler, uygulama kodunun düzenli ve sürdürülebilir olmasını sağlar.

### MVC (Model - View - Controller)

MVC mimarisinde uygulama üç katmana ayrılır:

- **Model:** Verileri ve iş mantığını içerir.
- **View:** Kullanıcıya gösterilen arayüzdür.
- **Controller:** Kullanıcı isteklerini işler ve Model ile View arasında iletişim kurar.

Akış:

```text
Kullanıcı
   ↓
Controller
   ↓
Model
   ↓
View
```

Web uygulamalarında sık kullanılır.

---

### MVVM (Model - View - ViewModel)

Özellikle modern frontend ve mobil uygulamalarda yaygındır.

- **Model:** Verileri ve iş mantığını içerir.
- **View:** Kullanıcı arayüzüdür.
- **ViewModel:** View ile Model arasında köprü görevi görür.

Akış:

```text
View ↔ ViewModel ↔ Model
```

React, Flutter, Android ve WPF gibi teknolojilerde benzer yaklaşımlar kullanılır.

---

## State Management Nedir?

State (durum), uygulamanın belirli bir andaki verileridir.

Örneğin:
- Kullanıcının giriş yapmış olması
- Sepetteki ürünler
- Tema ayarları
- Form verileri

State Management ise bu verilerin uygulama genelinde yönetilmesini sağlayan yaklaşımdır.

Avantajları:
- Veri tutarlılığı sağlar.
- Bileşenler arasında veri paylaşımını kolaylaştırır.
- Karmaşık uygulamaların yönetimini kolaylaştırır.

Popüler araçlar:
- Redux
- Context API
- Zustand
- MobX
- Vuex

---

## Katmanlı Mimari (Controller - Service - Repository)

Katmanlı mimari, uygulamanın sorumluluklarını farklı katmanlara ayırarak daha düzenli ve sürdürülebilir bir yapı oluşturur.

### Controller Katmanı

Kullanıcıdan gelen istekleri karşılar ve ilgili servisleri çağırır.

Örnek:

```http
GET /users
```

isteği Controller tarafından alınır.

---

### Service Katmanı

İş kurallarının bulunduğu katmandır.

Örneğin:
- Sipariş oluşturma
- İndirim hesaplama
- Yetkilendirme kontrolleri

gibi işlemler burada yapılır.

---

### Repository Katmanı

Veritabanı işlemlerini gerçekleştirir.

Örneğin:
- Veri ekleme
- Veri güncelleme
- Veri silme
- Veri sorgulama

işlemleri bu katmanda bulunur.

---

### Katmanlar Arasındaki Akış

```text
Client
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
Database
```

Bu yapı sayesinde kod daha okunabilir, test edilebilir ve sürdürülebilir hale gelir.

