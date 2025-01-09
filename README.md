# LCW-BootcampSql
### 1-test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

```sql
CREATE TABLE employee (
    id INTEGER PRIMARY KEY,
    name VARCHAR(50),
    birthday DATE,
    email VARCHAR(100)
);
```

### 2-Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```sql
INSERT INTO employee (id, name, birthday, email) VALUES
(1, 'Kelsey', '1954-08-13', 'kspaven0@google.fr'),
(2, 'Alissa', '1946-08-08', 'agaber1@imageshack.us'),
(3, 'Theodosia', '1973-06-27', 'tmish2@wordpress.org'),
(4, 'Miriam', '1932-09-09', 'mhaslum3@upenn.edu'),
(5, 'Gay', '1935-02-12', 'gliveing4@deliciousdays.com'),
(6, 'Kristoforo', '1971-03-17', 'kyellowley5@virginia.edu'),
(7, 'Reinhold', '1967-05-04', 'rizkovitz6@google.it'),
(8, 'Kristopher', '1968-11-29', 'khudleston7@blogspot.com'),
(9, 'Christan', '1942-07-31', 'cmarchington8@networksolutions.com'),
(10, 'Lorna', '1964-10-18', 'lcolleer9@w3.org'),
(11, 'Melania', '1935-12-11', 'mscaya@google.fr'),
(12, 'Sissy', '1949-08-13', 'sbunneyb@census.gov'),
(13, 'Selestina', '1968-04-26', 'srobartc@foxnews.com'),
(14, 'Jemimah', '1957-05-05', 'jtantumd@google.cn'),
(15, 'Aurora', '1944-08-11', 'aflippinie@webeden.co.uk'),
(16, 'Moyra', '1940-03-30', 'mpeevorf@europa.eu'),
(17, 'Traver', '1954-09-25', 'tcutressg@posterous.com'),
(18, 'Elysia', '1931-11-20', 'ereiglarh@dell.com'),
(19, 'Aindrea', '1965-11-03', 'akelleti@huffingtonpost.com'),
(20, 'Bonnee', '1974-11-23', 'bbodenj@mysql.com'),
(21, 'Myron', '1939-08-10', 'msedgerk@businessweek.com'),
(22, 'Farrah', '1961-10-27', 'ffeldbrinl@twitter.com'),
(23, 'Nissy', '1962-01-05', 'ncaustickm@msu.edu'),
(24, 'Terrye', '1938-01-18', 'trisboroughn@cbsnews.com'),
(25, 'Howard', '1958-10-21', 'hswateridgeo@gizmodo.com'),
(26, 'Ichabod', '1971-05-02', 'itribbeckp@time.com'),
(27, 'Benton', '1964-01-19', 'bmantrupq@ca.gov'),
(28, 'Giacobo', '1934-02-20', 'ginsworthr@cbc.ca'),
(29, 'Roseanna', '1943-10-25', 'rburghalls@yellowpages.com'),
(30, 'Wallace', '1970-03-31', 'wgusneyt@buzzfeed.com'),
(31, 'Gavra', '1962-05-20', 'gtrembletu@webeden.co.uk'),
(32, 'Bald', '1944-08-28', 'babreheartv@google.com.br'),
(33, 'Allyn', '1969-05-25', 'adulyw@unicef.org'),
(34, 'Greta', '1948-07-26', 'gvicarx@issuu.com'),
(35, 'Roseline', '1934-04-16', 'rhellmery@sun.com'),
(36, 'Goddart', '1932-06-14', 'gcyseleyz@si.edu'),
(37, 'Drusi', '1961-06-25', 'dperico10@phoca.cz'),
(38, 'Terese', '1972-05-21', 'tdarthe11@jimdo.com'),
(39, 'Colette', '1938-03-22', 'cjorg12@smh.com.au'),
(40, 'Clarine', '1938-06-24', 'cregenhardt13@skype.com'),
(41, 'Lorenzo', '1973-07-28', 'lwalles14@shop-pro.jp'),
(42, 'Christalle', '1951-05-14', 'cbathoe15@walmart.com'),
(43, 'Catherin', '1937-06-10', 'cwhittek16@cnet.com'),
(44, 'Allard', '1948-01-29', 'adurkin17@e-recht24.de'),
(45, 'Huey', '1954-06-22', 'hcullnean18@g.co'),
(46, 'Katha', '1963-12-25', 'ktuson19@umn.edu'),
(47, 'Sherry', '1949-09-15', 'sashard1a@telegraph.co.uk'),
(48, 'Gracie', '1970-11-03', 'gsmedmoor1b@is.gd'),
(49, 'Evan', '1930-09-05', 'eheaker1c@google.com.au'),
(50, 'Cull', '1951-05-19', 'csaxby1d@ibm.com');
```

### 3-Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```sql
-- id'ye göre güncelleme
UPDATE employee
SET name = 'Clair', birthday = '1954-07-17', email = 'clair@google.fr'
WHERE id = 1;

-- name'e göre güncelleme
UPDATE employee
SET birthday = '1990-01-01', email = 'lorenzo@shop.jp'
WHERE name = 'Lorenzo';

-- birthday'e göre güncelleme
UPDATE employee
SET name = 'Hagrid', email = 'hagrid@gizmodo.com'
WHERE birthday = '1958-10-21';

-- email'e göre güncelleme
UPDATE employee
SET name = 'Peter', birthday = '1853-02-12'
WHERE email = 'tmish2@wordpress.org';

-- sorguya göre güncelleme
UPDATE employee
SET name = UPPER(name)
WHERE birthday > '1970-01-01';
```

### 4-Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```sql
-- id ile silme
DELETE FROM employee
WHERE id = 22;

-- name ile silme
DELETE FROM employee
WHERE name = 'Gracie';

-- birthday ile silme
DELETE FROM employee
WHERE birthday = '1934-02-20';

-- email ile silme
DELETE FROM employee
WHERE email = 'tcutressg@posterous.com';

-- sorguya göre silme
DELETE FROM employee
WHERE birthday < '1960-01-01';
```




