### Step 6 - Working with Constraints

```
create table Users (
    create_date date,
    user_handle uuid,
    last_name text,
    first_name text,
    constraint PK_Users primary key (user_handle)
);
```

```
create table Users (
    create_date date not null,
    user_handle uuid not null unique,
    last_name text,
    first_name text not null
);
```