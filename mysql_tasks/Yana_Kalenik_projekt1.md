# Create a table with data

```sql
CREATE TABLE marvel_heroes (
    id INTEGER PRIMARY KEY,
    name TEXT,
    popularity INTEGER,
    alignment TEXT,
    gender TEXT, 
    height_m NUMERIC,
    weight_kg NUMERIC,
    hometown TEXT,
    intelligence INTEGER,
    strength INTEGER,
    speed INTEGER,
    durability INTEGER,
    energy_Projection INTEGER,
    fighting_Skills INTEGER);


INSERT INTO marvel_heroes VALUES(1, "Spider Man", 1, "Good", "Male", 1.78, 75.75, "USA", 4, 4, 3, 3, 1, 4); 
INSERT INTO marvel_heroes VALUES(2, "Iron Man", 20, "Neutral", "Male", 1.98, 102.58, "USA", 6, 6, 5, 6, 6, 4); 
INSERT INTO marvel_heroes VALUES(3, "Hulk", 18, "Neutral", "Male", 2.44, 635.29, "USA", 1, 7, 3, 7, 5, 4); 
INSERT INTO marvel_heroes VALUES(4, "Wolverine", 3, "Good", "Male", 1.6, 88.46, "Canada", 2, 4, 2, 4, 1, 7);
INSERT INTO marvel_heroes VALUES(5, "Thor", 5, "Good", "Male", 1.98, 290.3, "Asgard", 2, 7, 7, 6, 6, 4);
INSERT INTO marvel_heroes VALUES(6, "Green Goblin", 91, "Bad", "Male", 1.93, 174.63, "USA", 4, 4, 3, 4, 3, 3);
INSERT INTO marvel_heroes VALUES(7, "Magneto", 11, "Neutral", "Male", 1.88, 86.18, "Polish", 6, 3, 5, 4, 6, 4);
INSERT INTO marvel_heroes VALUES(8, "Thanos", 47, "Bad", "Male", 2.01, 446.79, "Titan", 6, 7, 7, 6, 6, 4);
INSERT INTO marvel_heroes VALUES(9, "Loki", 32, "Bad", "Male", 1.93, 238.14, "Jotunheim", 5, 5, 7, 6, 6, 3);
INSERT INTO marvel_heroes VALUES(10, "Doctor Doom", 19, "Bad", "Male", 2.01, 188.24, "Latveria", 6, 4, 5, 6, 6, 4);
INSERT INTO marvel_heroes VALUES(11, "Jean Grey", 8, "Good", "Female", 1.68, 52.16, "USA", 3, 2, 7, 7, 7, 4);
INSERT INTO marvel_heroes VALUES(12, "Rogue", 4, "Good", "Female", 1.73, 54.43, "USA", 7, 7, 7, 7, 7, 7);
INSERT INTO marvel_heroes VALUES(13, "Storm", 2, "Good", "Female", 1.80, 66, "Kenya", 2, 2, 3, 2, 5, 4);
INSERT INTO marvel_heroes VALUES(14, "Nightcrawler", 6, "Good", "Male", 1.75, 73, "Germany", 3, 2, 7, 2, 1, 3);
INSERT INTO marvel_heroes VALUES(15, "Gambit", 7, "Good", "Male", 1.88, 81, "EUA", 2, 2, 2, 2, 2, 4);
INSERT INTO marvel_heroes VALUES(16, "Captain America", 9, "Good", "Male", 1.88, 108, "EUA", 3, 3, 2, 3, 1, 6);
INSERT INTO marvel_heroes VALUES(17, "Cyclops", 10, "Good", "Male", 1.90, 88, "EUA", 3, 2, 2, 2, 5, 4);
INSERT INTO marvel_heroes VALUES(18, "Emma Frost", 12, "Neutral", "Female", 1.78, 65, "EUA", 4, 4, 2, 5, 5, 3);
INSERT INTO marvel_heroes VALUES(19, "Kitty Pryde", 13, "Good", "Female", 1.68, 50, "EUA", 4, 2, 2, 3, 1, 5);
INSERT INTO marvel_heroes VALUES(20, "Daredevil", 14, "Good", "Male", 1.83, 91, "EUA", 3, 3, 2, 2, 4, 5);
INSERT INTO marvel_heroes VALUES(21, "Punisher", 50, "Neutral", "Male", 1.85, 91, "EUA", 3, 3, 2, 2, 1, 6);
INSERT INTO marvel_heroes VALUES(22, "Silver Surfer", 33, "Good", "Male", 1.93, 102, "Zenn-La", 3, 7, 7, 6, 7, 2);
INSERT INTO marvel_heroes VALUES(23, "Ghost Rider", 86, "Good", "Male", 1.88, 99, "EUA", 2, 4, 3, 5, 4, 2);
INSERT INTO marvel_heroes VALUES(24, "Venom", 78, "Neutral", "Male", 1.90, 118, "EUA", 3, 4, 2, 6, 1, 4);
INSERT INTO marvel_heroes VALUES(25, "Juggernaut", 76, "Neutral", "Male", 2.87, 862, "EUA", 2, 7, 2, 7, 1, 4);
INSERT INTO marvel_heroes VALUES(26, "Professor X", 58, "Good", "Male", 1.83, 86, "EUA", 5, 2, 2, 2, 5, 3);
```

## Show  all rows from `marvel_heroes`
```sql
SELECT
    *
FROM
    marvel_heroes;
```


## What is the highest height in meters among the heroes?
```sql
SELECT
    MAX(height_m)
FROM
    marvel_heroes;
```
	
## The lowest intelligence among heroes	
```sql
SELECT
    MIN(intelligence)
FROM
    marvel_heroes;
```	

## Average popularity among heroes	
```sql
SELECT
    AVG(popularity)
FROM
    marvel_heroes;
```

## Select a hero with intelligence higher than 6, and show his hometown
```sql
SELECT
    COUNT(*) AS count,
    hometown,
    alignment
FROM
    marvel_heroes
WHERE
    intelligence > 6
GROUP BY
    hometown,
    alignment
ORDER BY
    hometown
```


## Select a average intelligence between heroes
```sql
SELECT
    AVG(intelligence) AS avg_int,
    hometown,
    alignment
FROM
    marvel_heroes
GROUP BY
    hometown,
    alignment
HAVING
    avg_int > 4
ORDER BY
    hometown;
```

## Show a female heroes with weight less than 70
```sql
SELECT
    *
FROM
    `marvel_heroes`
WHERE
    weight_kg < 70 AND gender = "Female";
```   
    
## Select heroes with a strong skills like durability, strength and speed
```sql
SELECT
    *
FROM
    `marvel_heroes`
WHERE
    durability > 5 OR strength > 5 OR speed > 5;
```   
    
## Select all heroes and create a new column to abbreviate their gender
```sql
SELECT
    id,
    gender,
    CASE WHEN gender = "Male" THEN "M" ELSE "F"
END abbrev
FROM
    marvel_heroes;
```    




