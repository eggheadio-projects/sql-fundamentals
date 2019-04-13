

## 1.
```sql
select * from Products where  price < '100.00';
```
| create_date              | product_id                           | title                                              | description                                      | price  |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ------------------------------------------------ | ------ |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | short React course                                 | This course you will start to learn about React. | $50.00 |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | short Vue course                                   | This course you will start to learn about Vue.   | $50.00 |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | short Angular course                               | This course you will start learning Angular.     | $50.00 |
---
## 2.
```sql
select * from Products where  title = 'SQL course';
```
| create_date              | product_id                           | title                                              | description                               | price   |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ----------------------------------------- | ------- |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | SQL course                                         | This course you will learn all about SQL. | $550.00 |

---
## Extra Credit
```sql
select * from Products where  title LIKE '%React%';
```
| create_date              | product_id                           | title                                              | description                                      | price   |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ------------------------------------------------ | ------- |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | short React course                                 | This course you will start to learn about React. | $50.00  |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | React course                                       | This course you will learn all about React.      | $150.00 |

---