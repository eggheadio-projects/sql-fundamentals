Our `Users` table currently has two rows of data, one for `danny clark` and a `debbie jones`. 
 
```sql 
select * from Users; 
  create_date |             user_handle              | last_name | first _name 
--------------+--------------------------------------+-----------+-------------
  2018-06-06  | 2839f831-f82c-faj3-aof3-fj28ddks39ek | clark     | danny  
  2018-1-06   | 6ab3b2d2-8e02-890c-bb6d-61a67cd43f31 | jones     | debbie  
  
(2 rows )
```

When we need to actually remove rows from our tables, instead of just updating column data, we'll use the `delete` command. If we don't put a `where` clause with our statement here, it's going to loop over each row over our table and delete everything. Make sure, before running the `delete` command on your table, you have a conditional clause that targets only the rows you want to delete. 

```sql 
delete from Users where last_name = 'clark';
DELETE 1
```

After defining which table we're removing rows from, we're saying, delete all the rows where the `last_name` column has a value of the text `clark`.

```sql 
select * from Users; 
  create_date |             user_handle              | last_name | first _name 
--------------+--------------------------------------+-----------+-------------
  2018-01-06  | 6ab3b2d2-8e02-890c-bb6d-61a67cd43f31 | jones     | debbie  
(1 rows )
```

We're also able to add other combinations of conditions here within the `where` clause. 
For example, we could say, `where last_name = 'clark' and first_name = 'danny';`, or even use the `or` statement instead of the `and` statement, as well. The key point here is, you want to make sure you're targeting the correct rows of data when deleting so that you don't actually lose the wrong rows. If you wanted to delete everything in our table, I mentioned you could just use the `delete` command without a condition.

However, using `truncate` is a more performant way to do so. 

```sql 
truncate Users;
TRUNCATE TABLE
```

```sql 
select * from Users; 
  create_date |             user_handle              | last_name | first _name 
--------------+--------------------------------------+-----------+-------------
(0 rows )
```

Unlike the `delete` command, it doesn't scan over the entire table. We also have the ability to `truncate` more than one table with just one statement by listing the other tables with commas.

Finally, if we're trying to remove the table completely from our database, we use the `drop` command. 

```sql 
drop table Users;
DROP TABLE
```

Once we run this command, all of the data is deleted and we cannot query anything from this table.

```sql 
select * from Users; 
ERROR: relation "users" does not exist
LINE 1: select * from Users;
```