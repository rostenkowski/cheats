PostgreSQL
----------

How to:

- Install the PostgreSQL database server and client.
- Login as the super-user.
- Create an admin account.
- Login as the admin-user.
- Create the project-database and the project-user.
- Grant all privileges on the project-database to the project-user.

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

MySQL
-----

Export database:

```bash
mysqldump -uroot -p database >> database.sql
```

Import database:

```bash
mysql -uroot -p -Ddatabase < database.sql
```