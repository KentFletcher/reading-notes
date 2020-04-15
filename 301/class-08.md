## SQL
***SQL***, or ***Structured Query Language***, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.
  - There are many popular SQL databases including SQLite, MySQL, Postgres, Oracle and Microsoft SQL Server. All of them support the common SQL language standard.   

A ***relational database*** represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.
### SELECT queries
***SELECT*** statements, or queries, are used to retrieve data from a SQL database.
  - A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. It has a specific syntax.

You can think of a table in SQL as a type of an entity (ie. Dogs), and each row in that table as a specific instance of that type (ie. A pug, a beagle, a different colored pug, etc). This means that the columns would then represent the common properties shared by all instances of that entity (ie. Color of fur, length of tail, etc).

Given a table of data, the most basic query we could write would be one that selects for a couple columns (properties) of the table with all the rows (instances).
  - SELECT column, another_column, …   
   FROM mytable;
  - The result of this query will be a two-dimensional set of rows and columns, effectively a copy of the table, but only with the columns that we requested.

If we want to retrieve absolutely all the columns of data from a table, we can then use the asterisk (*) shorthand in place of listing all the column names individually.
  - Select query for all columns  
SELECT *   
FROM mytable;
  - This query, in particular, is really useful because it's a simple way to inspect a table by dumping all the data at once.
### Queries with constraints 
In order to filter certain results from being returned, we need to use a ***WHERE*** clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.
- More complex clauses can be constructed by joining numerous ***AND*** or ***OR*** logical keywords (ie. num_wheels >= 4 AND doors <= 2).
  - Operators
    - =, !=, < <=, >, >= - Standard numerical operators
    - BETWEEN … AND … - Number is within range of two values (inclusive)
    - NOT BETWEEN … AND … - Number is not within range of two values (inclusive)
    - IN (…) - Number exists in a list
    - NOT IN (...) - Number does not exist in a list
- In addition to making the results more manageable to understand, writing clauses to constrain the set of rows returned also allows the query to run faster due to the reduction in unnecessary data being returned.
- When writing WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching.
  - =	Case sensitive exact string comparison (notice the single equals)
  - != or <>	Case sensitive exact string inequality comparison
  - LIKE	Case insensitive exact string comparison
  - NOT LIKE	Case insensitive exact string inequality comparison
  - %	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)
  - _	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)
  - IN (…)	String exists in a list
  - NOT IN (…)	String does not exist in a list
- All strings must be quoted so that the query parser can distinguish words in the string from SQL keywords.
- Select query with constraints  
SELECT column, another_column, …  
FROM mytable  
WHERE condition  
    AND/OR another_condition  
    AND/OR …;
### Filtering and sorting Query results
- Even though the data in a database may be unique, the results of any particular query may not be.  SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.
  - Select query with unique results  
SELECT DISTINCT column, another_column, …  
FROM mytable  
WHERE condition(s);
-  SQL provides a way to sort your results by a given column in ascending or descending order using the ORDER BY clause.
   - When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. In some databases, you can also specify a collation to better sort data containing international text.
   - Select query with ordered results  
SELECT column, another_column, …  
FROM mytable  
WHERE condition(s)  
ORDER BY column ASC/DESC;  

- Limiting results to a subset- Another clause which is commonly used with the ORDER BY clause are the LIMIT and OFFSET clauses, which are a useful optimization to indicate to the database the subset of the results you care about.
  - The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from.
  - Select query with limited rows  
SELECT column, another_column, …  
FROM mytable  
WHERE condition(s)  
ORDER BY column ASC/DESC  
LIMIT num_limit OFFSET num_offset;
### Schema
- In SQL, the database schema is what describes the structure of each table, and the datatypes that each column of the table can contain.
- This fixed structure is what allows a database to be efficient, and consistent despite storing millions or even billions of rows.
### Updating rows
- Update statement with values  
UPDATE mytable  
SET column = value_or_expr,   
    other_column = another_value_or_expr, …  
WHERE condition;
### Deleting rows
- Delete statement with condition  
DELETE FROM mytable  
WHERE condition;
- If you decide to leave out the WHERE constraint, then all rows are removed, which is a quick and easy way to clear out a table completely (if intentional).
### Creating tables
- Create table statement w/ optional table constraint and default value  
CREATE TABLE IF NOT EXISTS mytable (  
    column DataType TableConstraint DEFAULT default_value,  
    another_column DataType TableConstraint DEFAULT default_value,
    …  
);
- Table data types:
  - INTEGER, BOOLEAN
  - FLOAT, DOUBLE, REAL
  - CHARACTER(num_chars), VARCHAR(num_chars), TEXT
  - DATE, DATETIME
  - BLOB
- Table constraints
  - PRIMARY KEY
  - AUTOINCREMENT
  - UNIQUE
  - NOT NULL
  - CHECK (expression)
  - FOREIGN KEY