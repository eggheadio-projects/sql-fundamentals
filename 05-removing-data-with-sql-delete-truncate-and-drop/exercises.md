# Removing Data with SQL Delete, Truncate, and Drop Exercises

## Set up
<details>

<br>
If you created a `Products` table from a previous exercise, skip this query.

```sql
create table Products (
	create_date date,
  	product_id uuid,
  	title character(50),
  	description text,
  	price money,
   technology character(50)
);
```
Insert values into table:
```sql
insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'React course', 'This course you will learn all about React.', '150.00', 'react');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'Vue course', 'This course you will learn all about Vue.', '350.00', 'vue');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'Angular course', 'This course you will learn all about Angular.', '450.00', 'angular');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'SQL course', 'This course you will learn all about SQL.', '550.00', 'sql');
```
</details>


## 1. 

We no longer offer the React course. Delete this (where `title` equals `React course`) row from our `Products` table.

## 2.

Actually, we're getting rid of all our products. Delete every row in the `Products` table.

## 3. 

Lets make that perminate. Delete the `Products` table from our database.