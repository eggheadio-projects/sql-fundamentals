# Update Data in a Table with SQL Update Exercises

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

Update the `price` in the row where `title` is equal to `React course` to 300.00. 

## 2. 

Update the both the `price` and `description` of the row where `title` is equal to `SQL course`. 
