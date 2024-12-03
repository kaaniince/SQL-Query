`Soru1:` test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

```SQL
CREATE TABLE employee (
    id INTEGER PRIMARY KEY,
    name VARCHAR(50),
    birthday DATE,
    email VARCHAR(100)
);


```

`Soru2:` Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

```SQL
INSERT INTO employee (id, name, birthday, email) VALUES
(1, 'John Doe', '1985-04-12', 'john.doe@example.com'),
(2, 'Jane Smith', '1990-08-22', 'jane.smith@example.com'),
(3, 'Tom Brown', '1982-11-05', 'tom.brown@example.com'),
(4, 'Alice Green', '1995-02-19', 'alice.green@example.com'),
(5, 'Bob White', '1987-07-30', 'bob.white@example.com'),
(6, 'Emily Davis', '1991-01-17', 'emily.davis@example.com'),
(7, 'Michael Clark', '1980-12-25', 'michael.clark@example.com'),
(8, 'Sarah Lewis', '1993-04-14', 'sarah.lewis@example.com'),
(9, 'David Wilson', '1986-03-09', 'david.wilson@example.com'),
(10, 'Rebecca Walker', '1988-10-02', 'rebecca.walker@example.com'),
(11, 'James Martinez', '1994-06-30', 'james.martinez@example.com'),
(12, 'Laura Taylor', '1992-05-11', 'laura.taylor@example.com'),
(13, 'Daniel Anderson', '1983-08-03', 'daniel.anderson@example.com'),
(14, 'Sophia Thomas', '1997-12-18', 'sophia.thomas@example.com'),
(15, 'William Moore', '1984-09-07', 'william.moore@example.com'),
(16, 'Olivia Jackson', '1990-02-27', 'olivia.jackson@example.com'),
(17, 'Ethan Harris', '1981-10-21', 'ethan.harris@example.com'),
(18, 'Megan Martin', '1996-11-03', 'megan.martin@example.com'),
(19, 'Matthew Thompson', '1989-07-15', 'matthew.thompson@example.com'),
(20, 'Ava White', '1992-01-10', 'ava.white@example.com'),
(21, 'Alexander Robinson', '1984-04-04', 'alexander.robinson@example.com'),
(22, 'Charlotte Young', '1993-09-09', 'charlotte.young@example.com'),
(23, 'Samuel Scott', '1985-11-17', 'samuel.scott@example.com'),
(24, 'Chloe Adams', '1991-03-14', 'chloe.adams@example.com'),
(25, 'Jack King', '1980-12-11', 'jack.king@example.com'),
(26, 'Amelia Wright', '1994-07-01', 'amelia.wright@example.com'),
(27, 'Sebastian Lopez', '1987-02-10', 'sebastian.lopez@example.com'),
(28, 'Grace Gonzalez', '1995-05-06', 'grace.gonzalez@example.com'),
(29, 'Oliver Perez', '1990-08-08', 'oliver.perez@example.com'),
(30, 'Liam Carter', '1982-11-18', 'liam.carter@example.com'),
(31, 'Victoria Mitchell', '1991-10-25', 'victoria.mitchell@example.com'),
(32, 'Lucas Evans', '1996-04-03', 'lucas.evans@example.com'),
(33, 'Mia Green', '1993-07-21', 'mia.green@example.com'),
(34, 'Henry Rodriguez', '1988-02-14', 'henry.rodriguez@example.com'),
(35, 'Zoe Hall', '1984-01-30', 'zoe.hall@example.com'),
(36, 'Jacob Allen', '1986-09-04', 'jacob.allen@example.com'),
(37, 'Isabella Hernandez', '1997-12-01', 'isabella.hernandez@example.com'),
(38, 'Benjamin Nelson', '1992-06-18', 'benjamin.nelson@example.com'),
(39, 'Lily Carter', '1985-03-25', 'lily.carter@example.com'),
(40, 'Jackson Wright', '1990-10-12', 'jackson.wright@example.com'),
(41, 'Evelyn Adams', '1993-12-05', 'evelyn.adams@example.com'),
(42, 'Logan Baker', '1981-08-22', 'logan.baker@example.com'),
(43, 'Harper Gray', '1996-02-17', 'harper.gray@example.com'),
(44, 'Eli Mitchell', '1994-09-08', 'eli.mitchell@example.com'),
(45, 'Scarlett Harris', '1992-01-24', 'scarlett.harris@example.com'),
(46, 'Ryan Murphy', '1987-11-10', 'ryan.murphy@example.com'),
(47, 'Ella Lee', '1991-07-05', 'ella.lee@example.com'),
(48, 'David Moore', '1995-09-03', 'david.moore@example.com'),
(49, 'Landon Gonzalez', '1983-06-19', 'landon.gonzalez@example.com'),
(50, 'Charlie Black', '1980-01-01', 'charlie.black@example.com');


```

`Soru3:` Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

```SQL
UPDATE employee
SET name = 'Johnathan Doe'
WHERE id = 1;

UPDATE employee
SET birthday = '1992-03-15'
WHERE id = 2;

UPDATE employee
SET email = 'alice.green@newdomain.com'
WHERE id = 4;

UPDATE employee
SET id = 51
WHERE id = 50;

UPDATE employee
SET name = CONCAT(name, ' Updated')
WHERE birthday < '1990-01-01';

```

`Soru4:` Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

```SQL
DELETE FROM employee
WHERE name = 'Johnathan Doe';

DELETE FROM employee
WHERE birthday = '1995-02-19';

DELETE FROM employee
WHERE email = 'alice.green@newdomain.com';

DELETE FROM employee
WHERE id = 2;

DELETE FROM employee
WHERE birthday < '1990-01-01';


```
