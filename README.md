PostgreSQL
----------

```bash
sudo su postgres
psql
```
```sql
CREATE USER user WITH PASSWORD 'password' LOGIN;
CREATE DATABASE project;
GRANT ALL ON DATABASE project TO user;
```
Export SQL file:

```bash
sudo su postgres
pg_dump database > database.sql
```

Import SQL file:

```bash
sudo su postgres
psql -d database < file.sql 
```

MySQL
-----

```bash
mysql -u root -p
```
```sql
CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';
CREATE DATABASE project;
GRANT ALL PRIVILEGES ON project.* TO 'user'@'localhost';
FLUSH PRIVILEGES;
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
