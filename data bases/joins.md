# Joins in SQL

Joins are used to combine rows from two or more tables based on a related column. They allow retrieval of meaningful information by linking related data stored across different tables.

---

## Types of Joins

### 1. Inner Join
- Combines rows from both tables only when there is a match in the related column.
- Only matched rows appear in the result.
- **Example Scenario**: Listing all customers who have placed orders.

![Inner Join](media\img_inner_join.png)

---

### 2. Left Join (or Left Outer Join)
- Returns all rows from the left table, and the matched rows from the right table.
- If no match is found, the result includes rows from the left table with `NULL` for the right table columns.
- **Example Scenario**: Listing all customers, including those who have not placed any orders.


![Left Join](media\img_left_join.png)

---

### 3. Right Join (or Right Outer Join)
- Returns all rows from the right table, and the matched rows from the left table.
- If no match is found, the result includes rows from the right table with `NULL` for the left table columns.
- **Example Scenario**: Listing all orders, including those placed by unknown customers.

![Right Join](media\img_right_join.png)

---

### 4. Full Join (or Full Outer Join)
- Combines all rows from both tables.
- If no match is found, `NULL` is returned for columns from the other table.
- **Example Scenario**: Listing all customers and all orders, showing missing relationships.

![Full Join](media\img_full_outer_join.png)

---

### 5. Self Join
- A table is joined with itself to compare rows within the same table.
- Used for hierarchical data or comparing rows in the same dataset.
- **Example Scenario**: Finding employees who report to the same manager.

---

### 6. Cross Join (or Cartesian Join)
- Returns the Cartesian product of the two tables.
- Every row from the first table is paired with every row from the second table.
- **Example Scenario**: Generating all possible combinations of products and suppliers.

![cross Join](media\img_cross_join.png)

---

## Key Points
- Joins work using relationships between tables, often defined by primary and foreign keys.
- They help in creating complex queries to extract combined data.
- Choosing the right join depends on the scenario and desired output.

## **References**
- [Joins - W3 Schools](https://www.w3schools.com/sql/sql_join.asp)
- [Joins - GeeksforGeeks](https://www.geeksforgeeks.org/sql-join-set-1-inner-left-right-and-full-joins/)  
- [Joins - YouTube](https://youtu.be/4RmzfVUVxYI?si=mtPLDoWyVDDH43R7)