`Soru1:` actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.

```SQL
(
    SELECT a.first_name
    FROM actor a
)
UNION
(
    SELECT c.first_name
    FROM customer c;
)

```

`Soru2:` actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.

```SQL
(
    SELECT a.first_name
    FROM actor a
)
INTERSECT
(
    SELECT c.first_name
    FROM customer c;
)
```

`Soru3:` actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.

```SQL
(
    SELECT a.first_name
    FROM actor a
)
EXCEPT
(
    SELECT c.first_name
    FROM customer c;
)
```

`Soru4:` İlk 3 sorguyu tekrar eden veriler için de yapalım.

```SQL
(
    SELECT a.first_name
    FROM actor a
)

    UNION ALL

(
    SELECT c.first_name
    FROM customer c;
)
-----------------------------------------------
(
    SELECT a.first_name
    FROM actor a
)

    INTERSECT ALL

(
    SELECT c.first_name
    FROM customer c;
)
-----------------------------------------------
(
     SELECT a.first_name
    FROM actor a
)

    EXCEPT ALL

(
    SELECT c.first_name
    FROM customer c;
)
```
