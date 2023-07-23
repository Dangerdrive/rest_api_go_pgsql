# rest_api_go_pgsql

first I installed postgresql following the guidelines in https://www.postgresql.org/download/linux/ubuntu/

then we change the user to postgres (postgresql standard user)
```bash
$ sudo -i -u postgres
```
then to enter the client
```bash
$ psql
```
creating musicdb database and connecting to it
```bash
postgres=# CREATE DATABASE musicdb;
CREATE DATABASE
postgres=# \c musicdb;
You are now connected to database "musicdb" as user "postgres".
musicdb=# 
```

creating new table 
```bash
CREATE TABLE albums (
    ID TEXT PRIMARY KEY,
    Title TEXT,
    Artist TEXT,
    Price NUMERIC
);
```
```bash
INSERT INTO albums (id, title, artist, price) VALUES
    ('1', 'Blue Train', 'John Coltrane', 56.99),
    ('2', 'Jeru', 'Gerry Mulligan', 17.99),
    ('3', 'Sarah Vaughan and Clifford Brown', 'Sarah Vaughan', 39.99),
    ('4', 'Toe', 'New sentimentality', 21.99);
```

To verify data we can
SELECT * FROM albums;
