# Keep Data Integrity with Constraints Solutions

## 1.
```sql
create table Products (
 create_date date not null, 
 product_id uuid not null primary key,
 title character(50) not null,
 description text,
 price money not null,
 technology character(50) not null
); 
```