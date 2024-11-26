# **SQL and NoSql Databases**
## **SQL Basics Guide**
* **SQL** (Structured Query Language) is a programming language used to interact with relational databases. It allows you to **create, read, update, and delete** data. SQL is the foundation for many database systems, including MySQL, PostgreSQL, SQL Server, and SQLite.
* **Basic SQL Commands**
  * **SELECT - Querying Data :** The `SELECT` statement is used to retrieve data from a specific table.
  *  **INSERT - Adding New Data :** The `INSERT` Used to add a row (new data) to a table.
  *  **UPDATE - Modifying Data :** The `UPDATE` Used to update specific data in a table
  *  **DELETE  - Removing Data :** The `DELETE` Used to delete specific data from a table
  *  **JOIN - Linking Different Tables :** The ` JOIN ` Used to combine data from different tables based on a relationship between them.
     *  Types of JOIN:
        1. ` INNER JOIN ` : Returns rows that have matches in both tables

        2. ` LEFT JOIN ` : Returns all rows from the left table, and matched rows from the right table

        3. ` RIGHT JOIN ` : Returns all rows from the right table, and matched rows from the left table
---
# **NoSQL Database Guide**
* **Document-Oriented Databases**
Document-oriented databases store data in JSON-like documents. Each document is a self-contained unit of data, making it flexible for handling complex and hierarchical data structures.

* **Basic Syntax in Document Stores (MongoDB)**

  1. **Database Creation** (Implicit):
   - MongoDB automatically creates a database when data is inserted.
  
  2. **Insert Document**

  3. **Query Documents**
  
  4. **Update Document**

---

## When to Use SQL vs. NoSQL

- **Use SQL Databases** if you need:
  - To manage complex, interconnected data.
  - High data integrity and strict validation.
  - To handle critical transactions, like in banking or accounting systems.
  - Detailed reporting and analysis on fairly stable data.

- **Use NoSQL Databases** if you need:
  - To manage large volumes of constantly changing data (e.g., social media user data).
  - Support for easy and quick horizontal scaling.
  - Flexibility to store diverse, unstructured data.
  - Faster performance, even with relaxed consistency.


# **Additional Learning Resources**
-
- [sql , nosql video](https://youtu.be/eng2ZX78Oiw?si=hS3e_FXSvK6GWK-W)

- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/) : A comprehensive course for beginners explaining the basics and advanced SQL
  
- [MongoDB Documentation](https://www.mongodb.com/docs/manual/) : Comprehensive guide and tutorials on MongoDB.

- [Geeks for Geeks](https://www.geeksforgeeks.org/difference-between-sql-and-nosql/) a comparison between sql and no sql databases

