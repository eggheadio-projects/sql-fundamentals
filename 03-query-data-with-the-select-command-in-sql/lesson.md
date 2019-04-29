# Step 3 - Selecting Data

### Set up
```sql
create table Users (
    create_date date,
    user_handle uuid,
    last_name text,
    first_name text
);
```

```sql
insert into Users (create_date, user_handle, last_name, first_name ) values ('2018-06-06', 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'clark', 'tyler');
```

### Select all rows from Users Table
```
select * from Users;
```
| create_date              | user_handle                          | last_name | first_name |
| ------------------------ | ------------------------------------ | --------- | ---------- |
| 2018-06-06T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | clark     | tyler      |
| 2018-06-06T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | jones     | debbie     |

---

### Select all rows and current time from Users
```
select first_name, last_name, current_time from Users;
```
| first_name | last_name | current_time       |
| ---------- | --------- | ------------------ |
| tyler      | clark     | 14:24:36.817649+00 |
| debbie     | jones     | 14:24:36.817649+00 |

---
### Rename attributes on select
```
select first_name as FirstName, last_name as LastName, current_time as today from Users;
```
| firstname | lastname | today              |
| --------- | -------- | ------------------ |
| tyler     | clark    | 14:21:58.592996+00 |
| debbie    | jones    | 14:21:58.592996+00 |

---

### Select all rows with distinct last name
```
select distinct(last_name) from Users;
```
| last_name |
| --------- |
| clark     |
| jones     |

---

### Run aggregate functions on select statement
```sql
select count(distinct(last_name)) from Users;
                      
select count(last_name) from Users;
```
**First Query**
| count |
| ----- |
| 2     |
---
**Second Query**
| count |
| ----- |
| 3     |
