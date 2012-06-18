
Create PostgreSQL user:

```bash
sudo su postgres
psql
CREATE USER david WITH PASSWORD '*****';
```

Export MySQL database:

```bash
mysqldump -uroot -p database >> database.sql
```

Import MySQL database:

```bash
mysql -uroot -p -Ddatabase < database.sql
```