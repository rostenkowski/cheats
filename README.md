# PostgreSQL


```bash
sudo su postgres
psql
```
```sql
CREATE USER user WITH PASSWORD 'password' LOGIN;
CREATE DATABASE project;
GRANT ALL ON DATABASE project TO user;
```
## Export
```bash
pg_dump database > database.sql
```
## Import
```bash
psql -d database < file.sql 
```

# MySQL
```bash
mysql -u root -p
```
```sql
CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';
CREATE DATABASE project;
GRANT ALL PRIVILEGES ON project.* TO 'user'@'localhost';
FLUSH PRIVILEGES;
```
## Export
```bash
mysqldump -uroot -p database >> database.sql
```
## Import
```bash
mysql -uroot -p -Ddatabase < database.sql
```
## Reset root password
```bash
sudo dpkg-reconfigure mysql-server
```
