# Step 10 - Joining Tables


### Create a new table
```sql
create table Purchases (date date, user_handle uuid, sku uuid, quantity int);
```

### Create a row of data with user_handle
```sql
insert into Purchases (date, user_handle, sku, quantity) values ('2018-12-12', 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', uuid_generate_v4(), 2);
```

### Combine the User and Purchases table user handles
```sql
select * from Users u left outer join Purchases p on u.user_handle = p.user_handle;
```

### Create a row of data with random id's
```sql
insert into Purchases values ('2019-02-02', uuid_generate_v4(), uuid_generate_v4(), 1);
```

### Cross join the Users and Purchases table
```sql
select * from Users u cross join Purchases p;
```

### Combine the User and Purchases table emails
```sql
select * from Users u left outer join Purchases ua on u.email = ua.email;
```

