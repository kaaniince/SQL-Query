`Soru1:` film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

```SQL
SELECT AVG(rental_rate) AS average_rental_rate
FROM film;



```

`Soru2:` film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

```SQL
SELECT COUNT(*) AS count_c_titles
FROM film
WHERE title LIKE 'C%';




```

`Soru3:` film tablosunda bulunan filmlerden rental_rate değeri 0.99'a eşit olan en uzun (length) film kaç dakikadır?

```SQL
SELECT MAX(length) AS longest_film_length
FROM film
WHERE rental_rate = 0.99;

```

`Soru4:` film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

```SQL
SELECT COUNT(DISTINCT replacement_cost) AS distinct_replacement_costs
FROM film
WHERE length > 150;


```
