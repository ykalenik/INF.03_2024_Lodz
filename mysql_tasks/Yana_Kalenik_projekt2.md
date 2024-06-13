# Create a table with data
```sql
CREATE TABLE compositors (
	id INTEGER PRIMARY KEY, 
	name TEXT,
	country TEXT,
	composition TEXT,
	year_of_music INTEGER);
	
	
INSERT INTO compositors VALUES (1, "Giovanni Pierluigi da Palestrina", "Italy", "Benedictus", 1562);
INSERT INTO compositors VALUES (2, "Johann Sebastian Bach", "Germany", "Orchestral Suite No. 3 in D Major BWV 1068", 1723);
INSERT INTO compositors VALUES (3, "Wolfgang Amadeus Mozart", "Austria", "String Quartet No. 21, K. 575", 1789);
INSERT INTO compositors VALUES (4, "Johann Sebastian Bach", "Germany", "O Haupt Voll Blut Und Wunden", 1750);
INSERT INTO compositors VALUES (5, "Sergei Prokofiev", "Russia", "Montagues and Capulets", 1935);
INSERT INTO compositors VALUES (6, "Vittorio Monti", "Italy", "Csárdás", 1904);
INSERT INTO compositors VALUES (7, "Johann Sebastian Bach", "Germany", "Toccata and Fugue in D minor BWV 565", 1833);
INSERT INTO compositors VALUES (8, "Ludwig van Beethoven", "Germany", "Für Elise", 1810);
INSERT INTO compositors VALUES (9, "Ludwig van Beethoven", "Germany", "Sonata Pathétique №8", 1799);
INSERT INTO compositors VALUES (10, "Ludwig van Beethoven", "Germany", "Moonlight Sonata", 1801);
INSERT INTO compositors VALUES (11, "Frédéric Chopin", "Poland", "Prelude in E Minor Op. 28 No. 4", 1839);


CREATE TABLE covers (
	id INTEGER PRIMARY KEY, 
	artist TEXT,
	country TEXT,
	song TEXT,
	year_of_music INTEGER,
	compositors_id INTEGER);

INSERT INTO covers VALUES (1, "Muse", "England", "Drones", 2015, 1);
INSERT INTO covers VALUES (2, "Procol Harum", "England", "A Whiter Shade of Pale", 1967, 2);
INSERT INTO covers VALUES (3, "Clean Bandit", "England", "Mozart House", 2010, 3);
INSERT INTO covers VALUES (4, "Clean Bandit", "England", "A""+""E", 2012, 4);
INSERT INTO covers VALUES (5, "Sia", "Australia", "Taken ""for"" Granted", 2000, 5);
INSERT INTO covers VALUES (6, "Lady Gaga", "USA", "Alejandro", 2009, 6);
INSERT INTO covers VALUES (7, "Grace Jones", "Jamaica", "Autumn Leaves", 1978, 6);
INSERT INTO covers VALUES (8, "2""Unlimited", "Belgium", "The Real Thing", 1994, 7);
INSERT INTO covers VALUES (9, "Nas", "USA", "I Can", 2002, 8);
INSERT INTO covers VALUES (10, "Wu-Tang Clan ""&"" Tekitha", "USA","Impossible", 1997, 9);
INSERT INTO covers VALUES (11, "The Beatles", "England", "Because", 1969, 10);
INSERT INTO covers VALUES (12, "Alicia ""Keys""", "USA", "Piano ""&"" I", 2001, 10);
INSERT INTO covers VALUES (13, "Jane Birkin", "France", "Jane B", 1969, 11);


SELECT * FROM compositors INNER JOIN covers;

SELECT covers.artist, covers.song, compositors.name, compositors.composition FROM covers JOIN compositors ON covers.compositors_id = compositors.id;

SELECT covers.artist, covers.song, compositors.name, compositors.composition FROM covers JOIN compositors ON covers.compositors_id = compositors.id WHERE compositors.id = 10;

SELECT covers.artist, covers.song, compositors.name, compositors.composition FROM covers JOIN compositors ON covers.compositon_id = compositors.id WHERE compositors.country = "Germany";






```
