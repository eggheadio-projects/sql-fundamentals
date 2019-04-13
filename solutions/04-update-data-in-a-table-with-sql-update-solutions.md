# Update Data in a Table with SQL Update Solutions

## 1.
```sql
update Products set price = '300.00' where title = 'React course';
```
| create_date              | product_id                           | title                                              | description                                 | price   |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ------------------------------------------- | ------- |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | React course                                       | This course you will learn all about React. | $300.00 |

---

## 2.
```sql
update Products set price = '300.00', description = 'The new updated SQL course desctiption' where title = 'SQL course';
```
| create_date              | product_id                           | title                                              | description                            | price   |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | -------------------------------------- | ------- |
| 2019-04-11T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | SQL course                                         | The new updated SQL course desctiption | $300.00 |

---
