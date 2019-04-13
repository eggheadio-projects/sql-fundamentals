# Select Grouped and Aggregated Data with SQL Exercises

## Set up.
Up to this point we haven't had any constraints added to our data. We will need re-create the `Products` table with the constraints that we need.

Run `drop table Products` to get ready for this exercise.

## 1.
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
Modify the create statement above to ensure that all attributes (except the `description`) are always present in the database as well as setting the `product_id` as the primary key. 