# Veritabanı Mantığı (SQL Temelleri)

## Relational Database Nedir?

İlişkisel veritabanı (Relational Database), verilerin tablolar halinde saklandığı veritabanı modelidir. Her tablo satırlar (records) ve sütunlardan (columns) oluşur.

Tablolar arasında ilişkiler kurulabilir ve bu sayede veriler düzenli bir şekilde yönetilir.

Örneğin:

**Öğrenciler Tablosu**

| id | ad | bölüm |
|----|----|--------|
| 1 | Ali | Bilgisayar |
| 2 | Ayşe | Elektrik |

**Dersler Tablosu**

| id | ders_adi |
|----|----------|
| 1 | VeriYapilari |
| 2 | Algoritma |

Bu yapı sayesinde veriler tekrar etmeden saklanabilir ve kolayca sorgulanabilir.

---

## Primary Key ve Foreign Key

### Primary Key (Birincil Anahtar)

Bir tablodaki her kaydı benzersiz olarak tanımlayan sütundur.

Özellikleri:
- Tekrarlanamaz.
- Boş (NULL) olamaz.
- Her satır için benzersizdir.

Örnek:

| id | ad |
|----|----|
| 1 | Ali |
| 2 | Ayşe |

Burada `id` sütunu Primary Key'dir.

---

### Foreign Key (Yabancı Anahtar)

Bir tablodaki sütunun başka bir tablonun Primary Key'ine bağlanmasını sağlar.

Örnek:

**Öğrenciler**

| id | ad |
|----|----|
| 1 | Ali |
| 2 | Ayşe |

**Notlar**

| id | ogrenci_id | not |
|----|------------|-----|
| 1 | 1 | 90 |
| 2 | 2 | 85 |

Buradaki `ogrenci_id` sütunu Foreign Key'dir ve Öğrenciler tablosundaki `id` alanına bağlanır.

---

## SELECT – JOIN – GROUP BY Nedir?

### SELECT

Veritabanından veri çekmek için kullanılır.

Örnek:

```sql
SELECT * FROM ogrenciler;
```

Bu sorgu, öğrenciler tablosundaki tüm verileri getirir.

---

### JOIN

Birden fazla tabloyu ilişkilendirerek veri çekmek için kullanılır.

Örnek:

```sql
SELECT ogrenciler.ad, notlar.not
FROM ogrenciler
JOIN notlar
ON ogrenciler.id = notlar.ogrenci_id;
```

Bu sorgu öğrencilerin isimlerini ve notlarını birlikte getirir.

---

### GROUP BY

Verileri belirli alanlara göre gruplamak için kullanılır.

Örnek:

```sql
SELECT bolum, COUNT(*)
FROM ogrenciler
GROUP BY bolum;
```

Bu sorgu her bölümde kaç öğrenci olduğunu gösterir.

---

## Index Ne İşe Yarar?

Index (indeks), veritabanındaki aramaları hızlandırmak için kullanılan özel bir veri yapısıdır.

Bir kitabın sonundaki dizin mantığına benzer. Kitabın tamamını okumak yerine ilgili sayfaya doğrudan ulaşmayı sağlar.

Örneğin milyonlarca kayıt içeren bir tabloda:

```sql
SELECT *
FROM kullanicilar
WHERE email = 'ornek@mail.com';
```

sorgusunun hızlı çalışabilmesi için `email` alanına indeks eklenebilir.

Avantajları:
- Veri arama işlemlerini hızlandırır.
- Büyük veritabanlarında performansı artırır.
- Sorguların daha kısa sürede tamamlanmasını sağlar.

Dezavantajları:
- Ek depolama alanı kullanır.
- Veri ekleme ve güncelleme işlemlerini bir miktar yavaşlatabilir.