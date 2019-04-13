# Select Grouped and Aggregated Data with SQL Exercises

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
insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'short React course', 'This course you will start to learn about React.', '50.00', 'react');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'React course', 'This course you will learn all about React.', '150.00', 'react');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'short Vue course', 'This course you will start to learn about Vue.', '50.00', 'vue');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'Vue course', 'This course you will learn all about Vue.', '350.00', 'vue');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'short Angular course', 'This course you will start learning Angular.', '50.00', 'angular');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'Angular course', 'This course you will learn all about Angular.', '450.00', 'angular');

insert into Products values (now(), 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 'SQL course', 'This course you will learn all about SQL.', '550.00', 'sql');
```
</details>

## 1. 

Count up the `price` of all the products in our `Products` table.

Hint: You'll need to use a new aggregate function. Check out [the docs](https://www.postgresql.org/docs/11/functions-aggregate.html) to learn more.

## 2. 
Find the highest `price` for each given `technology` and display the `technology` with the `price`.