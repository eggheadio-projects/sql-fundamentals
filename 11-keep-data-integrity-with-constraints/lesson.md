### Step 11 - Subqueries

```
select u.total, u.create_date, first_name from Users us inner join (select count(create_date) as total, create_date from Users group by create_date) u on u.create_date = us.create_date;
```
```
select create_date, first_name from Users where create_date = (select min(create_date) from Users);
```
