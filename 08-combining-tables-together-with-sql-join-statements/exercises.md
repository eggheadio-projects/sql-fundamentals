# Combining Tables Together with SQL Join Statements Exercises

## Set up
It is important for these exercises that the id's (`user_handle` and `product_id`) match for the data that is put into the `Purchases` table. If you have data in your `Users` and `Products` already, you can delete that data and use what is provided below or grab the id's that you have set (they need to be unique).

Note: Purchase data available at the bottom of details section.
<details>
If data exists in the `Users` and `Products` tables: 
```sql
truncate Products;
truncate Users;
```

<br>
```sql
create table Users (
  create_date date,
  user_handle uuid,
  last_name text,
  first_name text
);
```
```sql
insert into Users (create_date, user_handle, last_name, first_name ) values ('2018-06-06', '4ff119f0-91b1-4020-8005-69bf0dd8b492', 'clark', 'tyler');
insert into Users (create_date, user_handle, last_name, first_name ) values ('2018-06-06', '6ab3b2d2-8e02-890c-bb6d-61a67cd43f31', 'jones', 'debbie');
insert into Users (create_date, user_handle, last_name, first_name ) values ('2018-06-06', '3bd67317-0efa-48c9-914c-42234072d94b', 'freemon', 'mary');
```

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

insert into Products values (now(), '5a2a8657-60d6-4d67-ac34-28f9a47a71d3', 'React course', 'This course you will learn all about React.', '150.00', 'react');

insert into Products values (now(), '13e55094-00d5-4c9b-bd8e-ce38072ae551', 'short Vue course', 'This course you will start to learn about Vue.', '50.00', 'vue');

insert into Products values (now(), '562951b6-3648-42fd-b49e-156c6a7edf60', 'Vue course', 'This course you will learn all about Vue.', '350.00', 'vue');

insert into Products values (now(), '18c299a8-772a-424b-841e-f3d082019271', 'short Angular course', 'This course you will start learning Angular.', '50.00', 'angular');

insert into Products values (now(), '40c88e1e-0910-4017-9b6f-12337e22183a', 'Angular course', 'This course you will learn all about Angular.', '450.00', 'angular');

insert into Products values (now(), '75f9eaba-136e-4b79-9579-5fd47b48797f', 'SQL course', 'This course you will learn all about SQL.', '550.00', 'sql');
```

```sql
create table Purchases (date date, user_handle uuid, sku uuid, quantity int);
```

```sql
insert into Purchases values ('2019-04-22', '4ff119f0-91b1-4020-8005-69bf0dd8b492', '75f9eaba-136e-4b79-9579-5fd47b48797f', 1);
insert into Purchases values ('2019-11-23', '4ff119f0-91b1-4020-8005-69bf0dd8b492', '40c88e1e-0910-4017-9b6f-12337e22183a', 3);
insert into Purchases values ('2019-07-02', '4ff119f0-91b1-4020-8005-69bf0dd8b492', '13e55094-00d5-4c9b-bd8e-ce38072ae551', 1);
insert into Purchases values ('2019-09-02', '4ff119f0-91b1-4020-8005-69bf0dd8b492', 'a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11', 2);
insert into Purchases values ('2019-05-23', '6ab3b2d2-8e02-890c-bb6d-61a67cd43f31', '75f9eaba-136e-4b79-9579-5fd47b48797f', 6);
insert into Purchases values ('2019-11-02', '6ab3b2d2-8e02-890c-bb6d-61a67cd43f31', '40c88e1e-0910-4017-9b6f-12337e22183a', 4);
insert into Purchases values ('2019-04-02', '4ff119f0-91b1-4020-8005-69bf0dd8b492', '40c88e1e-0910-4017-9b6f-12337e22183a', 2);
insert into Purchases values ('2019-11-02', '3bd67317-0efa-48c9-914c-42234072d94b', '75f9eaba-136e-4b79-9579-5fd47b48797f', 7);
insert into Purchases values ('2019-02-02', '3bd67317-0efa-48c9-914c-42234072d94b', '562951b6-3648-42fd-b49e-156c6a7edf60', 1);
insert into Purchases values ('2019-04-23', '4ff119f0-91b1-4020-8005-69bf0dd8b492', '5a2a8657-60d6-4d67-ac34-28f9a47a71d3', 1);
insert into Purchases values ('2019-04-02', '3bd67317-0efa-48c9-914c-42234072d94b', '18c299a8-772a-424b-841e-f3d082019271', 4);
insert into Purchases values ('2019-11-02', '4ff119f0-91b1-4020-8005-69bf0dd8b492', '562951b6-3648-42fd-b49e-156c6a7edf60', 1);
insert into Purchases values ('2019-10-23', '6ab3b2d2-8e02-890c-bb6d-61a67cd43f31', '5a2a8657-60d6-4d67-ac34-28f9a47a71d3', 3);
insert into Purchases values ('2019-04-12', '3bd67317-0efa-48c9-914c-42234072d94b', '13e55094-00d5-4c9b-bd8e-ce38072ae551', 1);
insert into Purchases values ('2019-02-15', '3bd67317-0efa-48c9-914c-42234072d94b', '5a2a8657-60d6-4d67-ac34-28f9a47a71d3', 2);
```
</details>


## 1.
Find all the `Products` that have been purchased and display the `title` and `date` of purchase


## 2. 

Find all `Products` that were purchased before `2019-06-15` with the `title`, `date`, and `quantity` displayed.

## 3.

Consider the [Postgres Table Expressions documentations](https://www.postgresql.org/docs/current/queries-table-expressions.html) and explore how you can join the tables you have created so far together.