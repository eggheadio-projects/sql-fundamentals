# Query Data with the Select Command in SQL Solutions

## 1.
```sql
select * from Products;
```
| create_date              | product_id                           | title                                              | description                                 | price   |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ------------------------------------------- | ------- |
| 2019-04-10T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | React course                                       | This course you will learn all about React. | $150.00 |
| 2019-04-10T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | Vue course                                         | This course you will learn all about Vue. | $350.00 |
| 2019-04-10T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | Angular course                                     | This course you will learn all about Angular. | $450.00 |
| 2019-04-10T00:00:00.000Z | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | SQL course                                         | This course you will learn all about SQL. | $550.00 |

---

## 2.
```sql
select count(*) from Products;
```
| count |
| ----- |
| 4     |

---

## 3.
```sql
select title from Products;
```
| title                                              |
| -------------------------------------------------- |
| React course                                       |
| Vue course                                         |
| Angular course                                     |
| SQL course                                         |

---
