PostgreSQL
----------

```bash
$ sudo su postgres
$ psql
> CREATE USER user WITH PASSWORD '***' LOGIN;
> CREATE DATABASE project;
> GRANT ALL ON DATABASE project TO user;
> ^D
```
Export SQL file:
```bash
pg_dump database > database.sql
```
Import SQL file:
```bash
psql -d database < file.sql 
```

MySQL
-----

```bash
$ mysql -u root -p
> CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';
> CREATE DATABASE project;
> GRANT ALL PRIVILEGES ON project.* TO 'user'@'localhost';
> FLUSH PRIVILEGES;
> ^D
```

Reset MySQL root password
```bash
sudo dpkg-reconfigure mysql-server
```

Export SQL file:

```bash
mysqldump -uroot -p database >> database.sql
```

Import SQL file:

```bash
mysql -uroot -p -Ddatabase < database.sql
```
