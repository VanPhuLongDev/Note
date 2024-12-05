1. What is a view in SQL?

**Answer:** A **view** in SQL is a virtual table that is based on the result of a query. It doesn't store data itself but displays data stored in other tables.


2. What are the types of JOINs in SQL?

**Answer:**
There are four main types of JOINs in SQL:

1. **INNER JOIN**: Returns only the rows that have matching values in both tables.
2. **LEFT JOIN (or LEFT OUTER JOIN)**: Returns all rows from the left table and the matched rows from the right table. If no match, NULL values are returned for columns from the right table.
3. **RIGHT JOIN (or RIGHT OUTER JOIN)**: Returns all rows from the right table and the matched rows from the left table. If no match, NULL values are returned for columns from the left table.
4. **FULL JOIN (or FULL OUTER JOIN)**: Returns all rows when there is a match in either the left or right table. If no match, NULL values are returned for the missing side.


3. What is an index in SQL?

**Answer:** An **index** in SQL is a database object that improves the speed of data retrieval operations on a table. It works like an index in a book, helping the database find rows more quickly. However, indexes can slow down write operations (like `INSERT`, `UPDATE`, and `DELETE`) because the index needs to be updated when data changes.

4. How does an index improve performance?

- **Answer:** An index speeds up data retrieval by allowing the database to quickly locate rows based on the indexed columns, rather than scanning the entire table. This is especially helpful in queries with `WHERE`, `JOIN`, or `ORDER BY` clauses.

5. What are the disadvantages of using indexes?

- **Answer:** The main disadvantages of indexes are:
    - Slower performance for `INSERT`, `UPDATE`, and `DELETE` operations because the index must be updated whenever the data changes.
    - Increased storage requirements to store the index structure.


6. How do you create an index in SQL?

- **Answer:** You can create an index using the `CREATE INDEX` statement:
    `CREATE INDEX idx_column_name ON table_name (column_name);`

7. What is a function in SQL?

**Answer:** A **function** in SQL is a set of instructions that do a specific task and return a result. It can be used to do things like calculate values, change data, or manipulate strings. Functions can be built-in (already provided by the database) or user-defined (created by you).

8. 