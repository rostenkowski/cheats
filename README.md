
Export MySQL database:

```bash
mysqldump -uroot -p database >> database.sql
```


Import MySQL database:

```bash
mysql -uroot -p -Ddatabase < database.sql
```