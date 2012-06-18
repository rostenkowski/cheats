PostgreSQL
----------

How to install the PostgreSQL database, login as the super-user, create an admin account, 
project database and project user and grant all privileges on the project database to the project user.

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
CREATE USER project WITH PASSWORD '***';
CREATE DATABASE project;
GRANT ALL ON DATABASE project TO project;
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