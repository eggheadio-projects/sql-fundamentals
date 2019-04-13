# Select Grouped and Aggregated Data with SQL Solutions

## 1. 
    select sum(price) from Products;

| sum       |
| --------- |
| $1,650.00 |

---



## 2.
    select max(price), technology from Products group by technology;

| max     | technology                                         |
| ------- | -------------------------------------------------- |
| $150.00 | react                                              |
| $450.00 | angular                                            |
| $550.00 | sql                                                |
| $350.00 | vue                                                |

---