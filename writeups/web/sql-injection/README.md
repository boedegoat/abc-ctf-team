# SQL Injection

**SQL Injection, basically a vulnerability where you can inject some raw sql query to manipulate database actions.**

```sql
-- Normal query
SELECT * FROM users WHERE username = 'admin' AND password = 'admin123'

-- After injecting
SELECT * FROM users WHERE username = '' OR 1=1 --' AND password = 'admin123'
```

Here are some useful stuff for performing sql injection:

**Comments:**

```sql
--
/**/
```

**End the query:**

```sql
;
```

**Concatenate strings:**

```sql
'ad' || 'min'
```

more stuff comming soon :sunglasses:
