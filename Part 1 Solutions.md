### Part 1 Exercises

Use SQL to create the following commands, and review the existing material.

1. Provide an SQL script to list all the available databases.

```sql
SHOW DATABASES;
```

2. Create a new database called `lab1_exercise_db`.

```sql
CREATE DATABASE lab1_exercise_db;
```

3. Select the `lab1_exercise_db` database as the current database to work.

```sql
use lab1_exercise_db;
```

4. Create a new table called `planets`, following the next data and specifications.

a. The table data includes the next:

| planet_id | planet_name | planet_terrain | planet_size |
| --------- | ----------- | -------------- | ----------- |
| A1        | Tatooine    | Desert         | 10465       |
| A2        | Coruscant   | Urban  area    | 6100        |

​	b. The table specification is as follows:

* `planet_id` is based on characters, and it is a primary key. This field will accept a maximum of 30 characters per input.
* `planet_name` is based on characters. This field will accept a maximum of 30 characters per input.
* `planet_terrain` is based on characters. This field will accept a maximum of 30 characters per input.
* `planet_size` is integer based.

5. Provide the SQL script to create the table.

```sql
CREATE TABLE planets(
    -> planet_id VARCHAR(30),
    -> planet_name VARCHAR (30),
    -> planet_terrain VARCHAR (30),
    -> planet_size INT,
    -> PRIMARY KEY (planet_id)
    -> );
```

6. Run a command to show the available tables.

```
SHOW TABLES;
```

7. Provide an SQL script to insert all the data into the `planets` table.

```sql
INSERT INTO
    -> planets
    -> VALUES
    -> ('A1','Tatooine','Desert',10465),
    -> ('A2', 'Coruscant','Urban area',6100);
```

8. Provide an SQL script to extract all the data and print it.

```mysql
SELECT * FROM planets;
```

9. Provide an SQL script to insert the following data.

| planet_id | planet_name  | planet_terrain | planet_size |
| --------- | ------------ | -------------- | ----------- |
| A3        | Death  Start | Urban  area    | 120         |

```sql
INSERT INTO planets VALUES ('A3','Death Start','Urban area',120);
```

10. Run the previous insert command once more. Does it fail, and why?

```mysql
INSERT INTO planets VALUES ('A3','Death Start','Urban area',120);
ERROR 1062 (23000): Duplicate entry 'A3' for key 'planets.PRIMARY'

--The command fails since a record with the same id already exists!--
```

11. Provide an SQL script to **extract all the data** and print it.

```mysql
SELECT * FROM planets;
```

12. Provide an SQL script to **extract all the planets** that have a size **greater than 5000** km.

```mysql
SELECT * FROM planets WHERE planet_size>5000;
```

13. Provide an SQL script to extract the planet names that have a **desert** terrain.

```mysql
SELECT planet_name FROM planets WHERE planet_terrain='Desert';
```

14. Provide an SQL script to **update** the size of the **Coruscant** planet to **6120**.

```mysql
UPDATE planets SET planet_size=6120 WHERE planet_id='A2';
```

15. Provide an SQL script to add a new column called `planet_population`. The new column should include **integers of up to 20 digits** in size.

```mysql
ALTER TABLE planets ADD planet_population INT(20);
```

16. Provide an SQL script to **update Tatooine's population to 200000**.

```mysql
UPDATE planets SET planet_population=200000 WHERE planet_id='A1';
```

17. Provide an SQL script to **delete the planet** `Death Star` from the table.

```mysql
DELETE FROM planets WHERE planet_id='A3';
```

18. Provide an SQL script to extract all the **planet names, terrains and sizes** for those **planets that start with the letter** `T`.

```mysql
SELECT * FROM planets WHERE planet_name LIKE 'T%';
```

:checkered_flag: Well done! 