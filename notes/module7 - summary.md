# A database schema defines how data is organized in a relational database. It includes:
- Tables: Row-and-column structures storing related data.
- Fields (Columns): Attributes of a record (e.g., MovieId, Title).
- Records (Rows): Individual entries in a table.
- Keys: Unique identifiers and references between tables.
- Relationships: How tables connect (one-to-one, one-to-many, many-to-many).
- Data Types: The format of data in each column (e.g., INT, VARCHAR).
Schemas help avoid redundancy and maintain data integrity.

# Keys 
- Primary Key (PK): A unique identifier for each record in a table (e.g., MovieId in the Movie table). Can be a single column or multiple columns combined.
- Foreign Key (FK): A column in one table that references the primary key in another table (e.g., MovieId in the Gross Income table links to the Movie table).
- Keys enable tables to be linked and data to be reconstructed across tables.

# Relationships 
1.	One-to-Many: One record in Table A relates to many records in Table B (e.g., one movie has many gross income entries).
2.	Many-to-Many: Records in Table A relate to many in Table B and vice versa (e.g., actors and movies). Requires a junction table.
3.	One-to-One: One record in Table A relates to exactly one record in Table B (e.g., a movie and its loan).

# Common Data Types 
- CHAR(size): Fixed-length string (max ~255 chars).
- VARCHAR(size): Variable-length string.
- TEXT: Long-form text.
- INT: Integer numbers.
- DECIMAL: Exact decimal numbers.
- FLOAT: Floating-point numbers.
- DATETIME: Date and time values.

# Why This Matters
Relational databases spread data across tables to reduce redundancy. Understanding schemas, keys, relationships, and data types is essential for:
- Writing effective SQL queries.
- Combining data from multiple tables.
- Maintaining data consistency and integrity.

# SQL JOIN Operations

## 1. Introduction to JOINs
- Relational databases store data across multiple interrelated tables
- JOIN operations allow retrieval of data from multiple tables simultaneously
- Tables are linked using primary and foreign keys (though any columns with matching data types can be used)

## 2. Basic JOIN Syntax
-SELECT table1.column1, table2.column2, ...
- FROM table1
- JOIN table2
    - ON table1.matching_column = table2.matching_column;
- AS creates aliases for table names (e.g., Review AS r)
  - ON clause specifies the join condition(s)

# Types of JOINs:
## A. INNER JOIN
- Returns only records with matching values in both tables
- Like the intersection in a Venn diagram
- Default behavior of JOIN keyword
- Note: "Water Bottle" (no match in bike_models) and "Racing ZY" (no match in bike_sales) are excluded

## B. LEFT JOIN (LEFT OUTER JOIN) 
- Returns all records from left table
- Returns matched records from right table
- NULL values for non-matching right table records

## C. RIGHT JOIN (RIGHT OUTER JOIN)
- Returns all records from right table
- Returns matched records from left table
- NULL values for non-matching left table records

## D. FULL OUTER JOIN (FULL JOIN)
- Returns all records from both tables
- NULL values where no matches exist

# NATURAL JOIN
- Automatically joins tables on columns with identical names and data types
- Produces same result as INNER JOIN but excludes duplicate columns
  - Important Caveats:
- Can produce incorrect results if columns with same name don't contain related data
- Common fields like "Modification_date" can interfere
- Safer to use INNER JOIN with explicit ON conditions

# Multiple Join Conditions:
- Required when composite keys are used
- Example:
- ON gi.movieId = gic.movieId 
   - AND gi.year = gic.year 
   - AND gi.month = gic.month

 # Joining More Than Two Tables:
- SELECT m.title, m.year, gi.year, gi.month, gic.Country, gic.Amount
- FROM Gross_Income AS gi
- JOIN Movie AS m ON m.movieId = gi.movieId
- JOIN Gross_Income_Country AS gic
    - ON gi.movieId = gic.movieId 
    - AND gi.year = gic.year 
    - AND gi.month = gic.month;
    
# Non-Key Joins:
- JOINs can use any columns with compatible data types, not just primary/foreign keys
- Example: Joining Person.date_birth with Review.date

# Visual Representation (Described in Text)
The material references Venn diagrams showing:
- Inner Join: Middle intersection only
- Left Join: Entire left circle + intersection
- Right Join: Entire right circle + intersection
- Full Outer Join: Both complete circles

# Important Notes:
- JOIN defaults to INNER JOIN
- Always verify column relationships when using NATURAL JOIN
- Table aliases improve query readability
- JOIN conditions should use indexed columns for performance
- Mismatched data types will cause join failures




