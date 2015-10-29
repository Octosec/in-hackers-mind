# Database

## Mysql

Connect to remote mysql server,
```bash
mysql -h <IP> -u <username> -p
```

Change user password,
```sql
SET PASSWORD FOR root@localhost = PASSWORD('newpassword');
```

Show databases, tables, fields,
```sql
SHOW DATABASES;
USE <db name>;
SHOW TABLES;
SHOW FIELDS FROM <table>;
```

Drop database,
```sql
DROP DATABASE <db name>;
```

Create database,
```sql
CREATE DATABASE <db name>;
GRANT ALL PRIVILEGES ON <db name>.* TO 'username' @ 'localhost' IDENTIFIED BY 'password';
SHOW GRANTS FOR 'username'@'localhost';
```

Select rows,
```sql
SELECT * FROM <table>;
SELECT * FROM <table> WHERE <field> = “value”;
```

Read file,
```sql
SELECT LOAD_FILE('/etc/passwd')\g;
```

Advance select,
```sql
ORDER BY <field> <ASC, DESC> 
GROUP BY <field>
LIMIT <number>
OFFSET <number>
```

## Postgresql

Connect remote host,
```bash
psql -h <IP> -U <username> -d <database> -W <password>
```

Get username, passwords,
```sql
select username, passwd from pg_shadow;
```

Read file,
```sql
create table test (input TEXT); copy test from '/etc/passwd'; select input from test;
```


