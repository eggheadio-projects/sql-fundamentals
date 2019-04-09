#  Create a Table with SQL Create Solution

### Product Table
```sql
create table Products (
  create_date date,
  product_id uuid,
  title character(50),
  description text,
  price money
);
```
To verify this works, add a product to the `Products` table with the `insert` command bellow:
```sql
insert into Products (create_date, product_id, title, description, price) values ('2018-06-06', 'b1debc99-9c0b-4ef8-bb6d-6bb9ac380bb1', 'sql course', 'This course is designed to take someone that has no experience with relational databases and teach them how to at least create, read, update, and delete.', '100.00');
```

And return all products from the table:
```sql
select * from Products;
```

This should produce output similar to: 

| create_date              | product_id                           | title                                              | description                                                                                                                                                                                                                                                                                                                                          | price   |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| 2018-06-06T00:00:00.000Z | b1debc99-9c0b-4ef8-bb6d-6bb9ac380bb1 | sql course                                         | This course is designed to take someone that has no experience with relational databases and teach them how to at least create, read, update, and delete. | $100.00 |

---