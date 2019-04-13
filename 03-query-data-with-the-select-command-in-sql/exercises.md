# Query Data with the Select Command in SQL Exercise

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

Select all products from the table.

## 2. 

How many products are in the `Products` table? Don't count manually. 😉

## 3.

Select all products and return only the course title.