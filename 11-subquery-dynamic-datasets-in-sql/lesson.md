# Step 11 - Subqueries
```sql
select create_date, first_name from Users where create_date = (select min(create_date) from Users);
```

or

```sql
select u.total, u.create_date, first_name from Users us inner join (select count(create_date) as total, create_date from Users group by create_date) u on u.create_date = us.create_date;
```

### Average between all purchases within the Purchases table
```sql
select user_handle, sku, (select avg(quantity) from Purchases) from Purchases;
```

### Return the first created User
```sql
select create_date, first_name from Users where create_date = (select min(create_date) from Users);
```
