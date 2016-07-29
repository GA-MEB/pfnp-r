[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : PostgreSQL

Let's talk about the concept of ‘persistence’, or storing data
outside a program. Data inside a program is not saved anywhere! We can write
data to text files, but this data isn’t necessarily easy to parse and search
through.

A **database** is a system for managing data. Data are written to files
(and read from those files) in such a way to maximize efficiency of storing
and searching/querying large amounts of data.

There are many different kinds of databases, but most common are ones that
follow the **SQL** standard (e.g. Postgres, MySQL). In a SQL database, data are
stored in tables of columns and rows, similar to a spreadsheet.
Unlike a spreadsheet, although rows can easily be added/removed/modified,
columns cannot be changed without scrapping your table, creating a new one,
and copying over (‘migrating’) the data over to the new table.

Think of it like having one table per sheet of paper.
Any time you want to change its structure, you need to take a new sheet,
create a new table with that structure, and copy over all the information.
A single database can have many different tables.

Generally, when we interact with databases, we do so through a database server
which listens for requests and reads from (or makes changes to) a given
database.

To launch Postgres as a service in Cloud9, go into the console and type

```bash
sudo service postgresql start
```

Once you do that, you'll be able to access Postgres through its CLI
client `psql`.

## `psql` Commands

Don’t waste time memorizing these commands -
focus on remembering where the reference pages are
and learning how to read and understand them.

### `CREATE DATABASE`

To create a new database, type `psql` in the console to open up the database
client, and inside the client, type `CREATE DATABASE myDatabase;`.
To destroy that database, write `DROP DATABASE myDatabase;`

The point of having a database is to manipulate tables and table rows,
so let's get to it.

### `CREATE`, `INSERT`, `SELECT`

You can create a new table and give it some rows by running

`CREATE TABLE people (name varchar, age integer, eye_color varchar);`

[reference : CREATE TABLE](https://www.postgresql.org/docs/9.3/static/datatype.html)

followed by

```sql
INSERT INTO people (name, age, eye_color) VALUES ('Matt', 29, 'hazel'),
('David', 33, 'brown');
```

[reference : INSERT](https://www.postgresql.org/docs/9.0/static/sql-insert.html)

Once you have some rows, you can try querying the database, to read back what
has been written there.

`SELECT * FROM people;`

`SELECT * FROM people WHERE name=’Matt’;`

`SELECT * FROM people WHERE age < 30;`

`SELECT * FROM people ORDER BY age (DESC);`

`SELECT name, age FROM people;`

[reference : SELECT](https://www.postgresql.org/docs/9.0/static/sql-select.html)

### UPDATE and DELETE

To update rows, use the ‘Update’ command

`UPDATE people SET age = age + 1;`

`UPDATE people SET age = 29 WHERE name=’Matt’;`

`UPDATE people SET age = 30 WHERE name='David' AND eye_color='blue'`

[reference : UPDATE](https://www.postgresql.org/docs/9.0/static/sql-update.html)

To delete rows, use ‘Delete’

`DELETE FROM people WHERE name=’David’;`

`DELETE FROM people WHERE age < 30;`

[reference : DELETE](https://www.postgresql.org/docs/9.0/static/sql-delete.html)
