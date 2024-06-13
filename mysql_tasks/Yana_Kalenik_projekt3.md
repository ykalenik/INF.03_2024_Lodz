# Create a table with data
```sql

CREATE TABLE dyolingo (
	id INTEGER PRIMARY KEY, 
	name TEXT,
	surname TEXT,
	nickname TEXT,
	age INTEGER,
	email TEXT,
	strike INTEGER,
	country TEXT);
	
INSERT INTO dyolingo VALUES(1, "Filip", "Sawyer", "Highbeam", 23, "kudra@verizon.net", 5, "France");
INSERT INTO dyolingo VALUES(2, "Shania", "Allison", "Terminator", 16, "zeitlin@msn.com", 100, "India");
INSERT INTO dyolingo VALUES(3, "Kamari","Lin", "Snow White", 46, "ivoibs@hotmail.com", 43, "China");
INSERT INTO dyolingo VALUES(4, "Sharon", "Gay", "Buddy", 14, "violinhi@mac.com", 56, "Canada");
INSERT INTO dyolingo VALUES(5, "Ethen", "Cuevas", "Dropout", 20, "maratb@hotmail.com", 236, "Portuguese");
INSERT INTO dyolingo VALUES(6, "Moises", "Hodge", "Captain", 56, "ribet@yahoo.ca", 1000, "Israel");
INSERT INTO dyolingo VALUES(7, "Deandre", "Little", "Elf",33, "tbusch@yahoo.ca", 432, "USA");
INSERT INTO dyolingo VALUES(8, "Alvaro", "Hess", "Short Shorts", 70, "codex@hotmail.com", 13, "Spain");
INSERT INTO dyolingo VALUES(9, "Sarai", "Hubbard", "Brutus", 27, "carroll@hotmail.com", 87, "Japan");
INSERT INTO dyolingo VALUES(10,"Mareli", "Osborne", "Candy", 12, "microfab@aol.com", 1475, "USA");
INSERT INTO dyolingo VALUES(11, "Xiomara", "Raymond", "Gordo", 18, "bjornk@yahoo.com", 187, "Germany");
INSERT INTO dyolingo VALUES(12, "Joseph", "Vaughan", "Betty Boop", 24, "tubesteak@yahoo.ca", 600,"Poland");


```

## Show table "dyolingo"
```
SELECT
    *
FROM
    `dyolingo`;

```

## Update email
```
UPDATE
    dyolingo
SET
    email = "marelosb@aol.com"
WHERE
    email = "microfab@aol.com";
```
## Delete from table
```
DELETE
FROM
    dyolingo
WHERE
    strike = 5;
```
## Show table "dyolingo"
```
SELECT
    *
FROM
    `dyolingo`;
```
