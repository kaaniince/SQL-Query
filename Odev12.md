`Soru1:` film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

```SQL
SELECT f.*
FROM film f
WHERE f.length > (
    SELECT AVG(f2.length)
    FROM film f2
)
ORDER BY f.length DESC;


```

`Soru2:` film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

```SQL
SELECT COUNT(*) AS film_count
FROM film f
WHERE f.rental_rate = (
    SELECT MAX(f2.rental_rate)
    FROM film f2
);

```

`Soru3:` film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

```SQL
SELECT f.*
FROM film f
WHERE f.replacement_cost = (
    SELECT MIN(f2.replacement_cost)
    FROM film f2
)
AND f.rental_rate = (
    SELECT MIN(f3.rental_rate)
    FROM film f3
);

```

`Soru4:` payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

```SQL
SELECT customer.customer_id, customer.first_name, customer.last_name, COUNT(payment.payment_id)
FROM customer
JOIN payment ON customer.customer_id = payment.customer_id
GROUP BY customer.customer_id
ORDER BY COUNT(payment.payment_id) DESC;

```
