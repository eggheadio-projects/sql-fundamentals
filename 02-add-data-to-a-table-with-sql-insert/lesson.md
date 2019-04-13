# 2 - Adding Data

### Create a Users Table
```sql
create table Users (
    create_date date,
    user_handle uuid,
    last_name text,
    first_name text
);
//-> CREATE TABLE
```

### Insert Data
```sql
insert into Users (create_date, user_handle, last_name, first_name ) values ('2018-06-06', 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'clark', 'tyler');
```

With built in postgres functions: 
```sql
insert into Users (create_date, user_handle, last_name, first_name ) values (now(), uuid_generate_v4(), 'johnson', 'patrick');
```

Shorthand:
```sql
insert into Users values (now(), uuid_generate_v4(), 'jones', 'zac');
```



