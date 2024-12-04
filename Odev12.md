`Soru1:` film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

```SQL
    SELECT * FROM film
    WHERE length >
    (
        SELECT AVG(length) FROM film
    );

```

`Soru2:` film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

```SQL
    SELECT COUNT(*) FROM film
    WHERE rental_rate =
    (
        SELECT MAX(rental_rate) FROM film
    );
```

`Soru3:` film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

```SQL
    SELECT * FROM film
    WHERE replacement_cost =
    (
        SELECT MIN(replacement_cost) FROM film
    )
    AND rental_rate =
    (
        SELECT MIN(rental_rate) FROM film
    )
```

`Soru4:` payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

```SQL
    SELECT customer.customer_id, customer.first_name, customer.last_name,COUNT(payment.payment_id)
    FROM customer
    JOIN payment ON customer.customer_id = payment.customer_id
    GROUP BY customer.customer_id
    ORDER BY COUNT(payment_id) DESC;
```
