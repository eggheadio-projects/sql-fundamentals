# Step 8 - Aggregate functions and grouping data

## Find the lowest value create_date in Table
```
select min(create_date), last_name, first_name from Users;
```

## Find the highest value create_date in Table
```
select max(create_date), last_name, first_name from Users;
```

## Count all users with the same last name
```
select count(*), last_name from Users group by last_name;
```