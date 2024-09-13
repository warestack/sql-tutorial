### Part 1 Exercises

Use SQL to create the following commands, and review the existing material.

1. Provide an SQL script to list all the available databases.

```sql
?
```

2. Create a new database called `lab1_exercise_db`.

```sql
?
```

3. Select the `lab1_exercise_db` database as the current database to work.

```sql
?
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
?
```

6. Run a command to show the available tables.

```
?
```

7. Provide an SQL script to insert all the data into the `planets` table.

```sql
?
```

8. Provide an SQL script to extract all the data and print it.

```mysql
?
```

9. Provide an SQL script to insert the following data.

| planet_id | planet_name  | planet_terrain | planet_size |
| --------- | ------------ | -------------- | ----------- |
| A3        | Death  Start | Urban  area    | 120         |

```mysql
?
```

10. Run the previous insert command once more. Does it fail, and why?

```mysql
?
```

11. Provide an SQL script to **extract all the data** and print it.

```mysql
?
```

12. Provide an SQL script to **extract all the planets** that have a size **greater than 5000** km.

```mysql
?
```

13. Provide an SQL script to extract the planet names that have a **desert** terrain.

```mysql
?
```

14. Provide an SQL script to **update** the size of the **Coruscant** planet to **6120**.

```mysql
?
```

15. Provide an SQL script to add a new column called `planet_population`. The new column should include **integers of up to 20 digits** in size.

```mysql
?
```

16. Provide an SQL script to **update Tatooine's population to 200000**.

```mysql
?
```

17. Provide an SQL script to **delete the planet** `Death Star` from the table.

```mysql
?
```

18. Provide an SQL script to extract all the **planet names, terrains and sizes** for those **planets that start with the letter** `T`.

```mysql
?
```

:checkered_flag: Well done! 