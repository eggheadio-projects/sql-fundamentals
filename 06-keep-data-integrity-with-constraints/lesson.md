# Step 6 - Working with Constraints

## Create a Users table with Primary key set to user_handle
```
create table Users (
    create_date date,
    user_handle uuid,
    last_name text,
    first_name text,
    constraint PK_Users primary key (user_handle)
);
```

## Create a Users table where no values can be null (except `last_name`) and the `user_handle` as unique
```sql
create table Users (
    create_date date not null,
    user_handle uuid not null unique,
    last_name text,
    first_name text not null
);
```

## Create a table with a foreign key
```sql
create table Purchases (
  date date not null, 
  user_handle uuid references Users (user_handle),
  sku uuid not null,
  quantity int not null, 
); 
```