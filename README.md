PostgreSQL
----------

```bash
$ whoami 
joe
$ sudo apt-get install postgresql
$ sudo su postgres
$ psql
> CREATE DATABASE joe;
> CREATE USER joe WITH PASSWORD '***' CREATEDB CREATEUSER LOGIN;
> GRANT ALL ON DATABASE joe TO joe;
^D
$ ^D
$ psql  
> CREATE USER project WITH PASSWORD '***' LOGIN;
> CREATE DATABASE project;
> GRANT ALL ON DATABASE project TO project;
^D
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
