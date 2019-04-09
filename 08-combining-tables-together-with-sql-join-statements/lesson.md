### Step 8 - Aggregate functions and grouping data

```
select min(create_date), last_name, first_name from Users;
```

```
select max(create_date), last_name, first_name from Users;
```

```
select count(*), last_name from Users group by last_name;
```