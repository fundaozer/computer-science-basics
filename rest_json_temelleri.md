# API Mantığı (REST & JSON Temelleri)

## API Nedir, Neden Var?

API (Application Programming Interface), farklı yazılımların birbiriyle iletişim kurmasını sağlayan bir arayüzdür. Bir uygulamanın sunduğu verileri veya hizmetleri başka uygulamaların kullanabilmesine olanak tanır.

Örneğin bir hava durumu uygulaması, hava durumu verilerini bir API üzerinden alabilir.

API'lerin temel amacı:
- Uygulamalar arasında veri alışverişi sağlamak
- Sistemlerin birbirleriyle haberleşmesini kolaylaştırmak
- Yazılım geliştirme sürecini hızlandırmak

---

## GET – POST – PUT – DELETE

REST API'lerde en yaygın kullanılan HTTP metodları şunlardır:

- **GET:** Sunucudan veri almak için kullanılır.
- **POST:** Sunucuya yeni veri göndermek ve oluşturmak için kullanılır.
- **PUT:** Var olan bir veriyi güncellemek için kullanılır.
- **DELETE:** Bir veriyi silmek için kullanılır.

Örnek:

```http
GET /users
POST /users
PUT /users/1
DELETE /users/1
```

---

## JSON Yapısı

JSON (JavaScript Object Notation), verilerin istemci ve sunucu arasında taşınmasını sağlayan hafif ve okunabilir bir veri formatıdır.

Örnek JSON:

```json
{
  "id": 1,
  "ad": "Funda",
  "yas": 20,
  "bolum": "Bilgisayar Mühendisliği"
}
```

JSON günümüzde web servisleri ve API'lerde en yaygın kullanılan veri formatlarından biridir.

---

## Basit Bir Endpoint Nasıl Tasarlanır?

Endpoint, API içerisinde belirli bir kaynağa erişmek için kullanılan URL'dir.

Örnek bir kullanıcı API'si:

```http
GET /users
```

Tüm kullanıcıları getirir.

```http
GET /users/1
```

ID'si 1 olan kullanıcıyı getirir.

```http
POST /users
```

Yeni bir kullanıcı oluşturur.

Basit bir endpoint tasarlanırken:
- URL'ler anlaşılır olmalıdır.
- Kaynak isimleri çoğul kullanılmalıdır (`users`, `products` gibi).
- HTTP metodları doğru seçilmelidir.
- Dönen veriler genellikle JSON formatında olmalıdır.

---