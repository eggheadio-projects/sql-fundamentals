# Add Data to a Table with SQL Insert Exercises

In the previous exercise, you created a Products table, check the `solutions.md` file in the [01-create-a-table-with-sql-create](../01-create-a-table-with-sql-create/solutions.md) folder to create a `Products` table for this exercise

In the lesson, you inserted data into the `User` table.

Lets do the same for `Products`.

## 1. Add Static Data to Products table

You'll need a `create_date`, `product_id`, `title`, `description`, `price`, and `technology`.

Here's some data you can use:
```
2019-04-09

407b4a99-e4fe-437b-9ce9-8ebe84e0a014

sql fundamentals course

This course is designed to take someone that has no experience with relational databases and teach them how to at least create, read, update, and delete.

100.00

sql
```

## 2. Add Dynamic Data Products table

Some attibutes like `create_date` and `product_id` you don't want to generate yourself.

Check out the [now](https://www.postgresql.org/docs/11/functions-datetime.html) and [uuid](https://www.postgresql.org/docs/11/uuid-ossp.html) function pages to see how you can have postgres generate these values for you.

HINT:  If you see this error:

`No function matches the given name and argument types. You might need to add explicit type casts.`

when using the `uuid` functuion you find, check out this [stack overflow post](https://stackoverflow.com/questions/43685799/postgres-uuid-type-error) for the solution.