`Soru1:` city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

```SQL
SELECT city.city AS CityName, country.country AS CountryName
FROM city
INNER JOIN country
ON city.country_id = country.country_id;
```

`Soru2:` customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

```SQL
SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN payment
ON customer.customer_id = payment.customer_id;

```

`Soru3:` customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

```SQL
SELECT rental.rental_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN rental
ON customer.customer_id = rental.customer_id;

```