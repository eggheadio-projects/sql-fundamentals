## 1.
```sql
select p.title as Product, pp.date as DatePurchased from Products p left outer join Purchases pp on p.product_id = pp.sku;
```
| product                                            | datepurchased            |
| -------------------------------------------------- | ------------------------ |
| SQL course                                         | 2019-04-22T00:00:00.000Z |
| Angular course                                     | 2019-11-23T00:00:00.000Z |
| short Vue course                                   | 2019-07-02T00:00:00.000Z |
| short React course                                 | 2019-09-02T00:00:00.000Z |
| SQL course                                         | 2019-05-23T00:00:00.000Z |
| Angular course                                     | 2019-11-02T00:00:00.000Z |
| Angular course                                     | 2019-04-02T00:00:00.000Z |
| SQL course                                         | 2019-11-02T00:00:00.000Z |
| Vue course                                         | 2019-02-02T00:00:00.000Z |
| React course                                       | 2019-04-23T00:00:00.000Z |
| short Angular course                               | 2019-04-02T00:00:00.000Z |
| Vue course                                         | 2019-11-02T00:00:00.000Z |
| React course                                       | 2019-10-23T00:00:00.000Z |
| short Vue course                                   | 2019-04-12T00:00:00.000Z |
| React course                                       | 2019-02-15T00:00:00.000Z |

---

## 2. 
```sql
select p.title as Product, pp.date as DatePurchased, pp.quantity from Products p left outer join Purchases pp on p.product_id = pp.sku where pp.date < '2019-06-15';
```
| product                                            | date                     | quantity     |
| -------------------------------------------------- | ------------------------ | ------------ |
| SQL course                                         | 2019-04-22T00:00:00.000Z | 1            |
| SQL course                                         | 2019-05-23T00:00:00.000Z | 6            |
| Angular course                                     | 2019-04-02T00:00:00.000Z | 2            |
| Vue course                                         | 2019-02-02T00:00:00.000Z | 1            |
| React course                                       | 2019-04-23T00:00:00.000Z | 1            |
| short Angular course                               | 2019-04-02T00:00:00.000Z | 4            |
| short Vue course                                   | 2019-04-12T00:00:00.000Z | 1            |
| React course                                       | 2019-02-15T00:00:00.000Z | 2            |

---