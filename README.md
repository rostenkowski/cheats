Create PostgreSQL user:

```bash
sudo su postgres
psql
CREATE USER root WITH PASSWORD '*****';
GRANT ALL PRIVILEGES ON database TO root; -- WITH ADMIN OPTION to create super-user
```

Export MySQL database:

```bash
mysqldump -uroot -p database >> database.sql
```

Import MySQL database:

```bash
mysql -uroot -p -Ddatabase < database.sql
```