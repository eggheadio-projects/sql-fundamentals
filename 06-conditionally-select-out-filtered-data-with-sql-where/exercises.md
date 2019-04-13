# Conditionally Select out Filtered Data with SQL Where Exercises

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

You are looking for an intro to a few technologies. Filter for all courses with a price less than 100.00.

## 2.

You're looking for a specific course. Filter for rows where `title` is equal to `SQL course`

## Extra Credit

You've decided you only want to look at react courses. Filter for titles that include `React`. 

Hint: You might want to use [a new operator](https://stackoverflow.com/questions/14290857/sql-select-where-field-contains-words)