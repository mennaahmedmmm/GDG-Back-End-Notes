# **Database Keys**

## **What is a Key?**
A `key` is a field or set of fields that `uniquely identifies` a `record` in a table. Keys are used to `retrieve records` from a database table according to different `access paths`.

## **Types of Keys**
![Database Keys](./media/database_keys.png "A title")

1. **Primary Key**:  
   A field in a table that `uniquely identifies` each row/record.  
   - Must contain `unique values`.  
   - Cannot have `NULL` values.

2. **Unique Key**:  
   A set of one or more fields/columns that `uniquely identifies` a record.  
   - Similar to a `primary key`.  
   - Used to avoid `data duplication`.

3. **Super Key**:  
   A set of one or more keys used to `uniquely identify` a record in a table.  
   - May contain `additional attributes` that are not strictly required for unique identification.

4. **Candidate Key**:  
   A set of one or more fields/columns that can be used as a `primary key`.  
   - A `super key` with no repeated attributes.

5. **Foreign Key**:  
   A field in a table that is a `primary key` in another table.  
   - Used to `link` two tables together.

6. **Composite Key**:  
   A `combination` of two or more columns that can `uniquely identify` each record in a table.  
   - Also known as a `compound key`.

7. **Natural Key**:  
   A key formed from `existing data` in the database table.  
   - Sometimes called a `domain key`.

8. **Surrogate Key**:  
   A `unique identifier` for an entity or object in the database.  
   - A system-generated value that is guaranteed to be `unique`.

9. **Alternate Key**:  
   A key that can be used as a `primary key`.  
   - A `candidate key` not selected as the primary key of the table.
---

## **References**
- [Types of Keys in Relational Model - GeeksforGeeks](https://www.geeksforgeeks.org/types-of-keys-in-relational-model-candidate-super-primary-alternate-and-foreign/)  
- [Types of Keys in Database - YouTube](https://youtu.be/8wUUMOKAK-c?si=p1Z8TBAEMWxBbwl8)
