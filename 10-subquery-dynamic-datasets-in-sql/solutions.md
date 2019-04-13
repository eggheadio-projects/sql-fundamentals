## 1. 
```sql
select user_handle, sku, (select avg(quantity) from Purchases where user_handle = p.user_handle and sku = p.sku) from Purchases p group by user_handle, sku;
```
| user_handle                          | sku                                  | avg                    |
| ------------------------------------ | ------------------------------------ | ---------------------- |
| 3bd67317-0efa-48c9-914c-42234072d94b | 75f9eaba-136e-4b79-9579-5fd47b48797f | 7.0000000000000000     |
| 4ff119f0-91b1-4020-8005-69bf0dd8b492 | 40c88e1e-0910-4017-9b6f-12337e22183a | 2.5000000000000000     |
| 4ff119f0-91b1-4020-8005-69bf0dd8b492 | 75f9eaba-136e-4b79-9579-5fd47b48797f | 1.00000000000000000000 |
| 3bd67317-0efa-48c9-914c-42234072d94b | 5a2a8657-60d6-4d67-ac34-28f9a47a71d3 | 2.0000000000000000     |
| 4ff119f0-91b1-4020-8005-69bf0dd8b492 | 5a2a8657-60d6-4d67-ac34-28f9a47a71d3 | 1.00000000000000000000 |
| 4ff119f0-91b1-4020-8005-69bf0dd8b492 | a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11 | 2.0000000000000000     |
| 3bd67317-0efa-48c9-914c-42234072d94b | 13e55094-00d5-4c9b-bd8e-ce38072ae551 | 1.00000000000000000000 |
| 6ab3b2d2-8e02-890c-bb6d-61a67cd43f31 | 75f9eaba-136e-4b79-9579-5fd47b48797f | 6.0000000000000000     |
| 4ff119f0-91b1-4020-8005-69bf0dd8b492 | 13e55094-00d5-4c9b-bd8e-ce38072ae551 | 1.00000000000000000000 |
| 6ab3b2d2-8e02-890c-bb6d-61a67cd43f31 | 40c88e1e-0910-4017-9b6f-12337e22183a | 4.0000000000000000     |
| 4ff119f0-91b1-4020-8005-69bf0dd8b492 | 562951b6-3648-42fd-b49e-156c6a7edf60 | 1.00000000000000000000 |
| 3bd67317-0efa-48c9-914c-42234072d94b | 562951b6-3648-42fd-b49e-156c6a7edf60 | 1.00000000000000000000 |
| 3bd67317-0efa-48c9-914c-42234072d94b | 18c299a8-772a-424b-841e-f3d082019271 | 4.0000000000000000     |
| 6ab3b2d2-8e02-890c-bb6d-61a67cd43f31 | 5a2a8657-60d6-4d67-ac34-28f9a47a71d3 | 3.0000000000000000     |

---
## 2. 
```sql
select total, title from Products pr inner join (select count(sku) as total, sku from Purchases group by sku) p on p.sku = pr.product_id;
```
| total | title                                              |
| ----- | -------------------------------------------------- |
| 1     | short React course                                 |
| 3     | React course                                       |
| 2     | short Vue course                                   |
| 2     | Vue course                                         |
| 1     | short Angular course                               |
| 3     | Angular course                                     |
| 3     | SQL course                                         |

---