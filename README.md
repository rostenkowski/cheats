Create PostgreSQL super-user, create database and regular user and grant privileges to the regular user:

```bash
$ whoami 
joe
$ sudo apt-get install postgresql
$ sudo su postgres
$ psql
CREATE USER joe WITH PASSWORD '***' CREATEDB CREATEUSER;
\q
$ exit
$ psql  
CREATE DATABASE project;
GRANT ALL ON DATABASE project TO joe;
\q
```

Export MySQL database:

```bash
mysqldump -uroot -p database >> database.sql
```

Import MySQL database:

```bash
mysql -uroot -p -Ddatabase < database.sql
```