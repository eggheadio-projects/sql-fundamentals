# Step 9 - Filtering Data

### Filter on last name
```
select create_date, last_name, first_name from Users where last_name = 'clark';
```

### Filter on a Date Range
```
select * from Users where create_date between '2018-05-01' and '2018-09-01';
```