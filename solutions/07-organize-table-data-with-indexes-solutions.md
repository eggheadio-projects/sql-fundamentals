## 1.
```sql
create index test1_product_id_index on Products (product_id);
```

## 2. 
```sql
\d Products
```
Table "public.products"
| Column                  | Type          | Collation   | Nullable    | Default     |
| ----------------------- | --------------| ----------- | ----------- | ----------- |
| create_date             | date          |             |             |             |
| product_id              | uuid          |             |             |             |
| title                   | character     |             |             |             |
| description             | text          |             |             |             |
| price                   | money         |             |             |             |
| technology              | character     |             |             |             |

Indexes: "test1_product_id_index" btree (product_id)
                   
## 3. 
```sql
create index test1_product_id_and_technology_index on Products (product_id, technology);
```
Table "public.products"
| Column                  | Type          | Collation   | Nullable    | Default     |
| ----------------------- | --------------| ----------- | ----------- | ----------- |
| create_date             | date          |             |             |             |
| product_id              | uuid          |             |             |             |
| title                   | character     |             |             |             |
| description             | text          |             |             |             |
| price                   | money         |             |             |             |
| technology              | character     |             |             |             |

Indexes: 
"test1_product_id_and_technology_index" btree (product_id, technology)
"test1_product_id_index" btree (product_id)