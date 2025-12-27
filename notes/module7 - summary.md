# Database Fundamentals, SQL JOINs & NoSQL Systems

## Database Schema
A database schema defines how data is organized in a relational database. It includes:

- Tables: Row-and-column structures storing related data
- Fields (Columns): Attributes of a record (e.g., MovieId, Title)
- Records (Rows): Individual entries in a table
- Keys: Unique identifiers and references between tables
- Relationships: How tables connect (one-to-one, one-to-many, many-to-many)
- Data Types: The format of data in each column (e.g., INT, VARCHAR)

Schemas help avoid redundancy and maintain data integrity.

---

## Keys

### Primary Key (PK)
A unique identifier for each record in a table.
- Example: MovieId in the Movie table
- Can be a single column or a composite key

### Foreign Key (FK)
A column in one table that references the primary key in another table.
- Example: MovieId in the Gross_Income table links to the Movie table

Keys enable tables to be linked and data to be reconstructed across tables.

---

## Relationships

### One-to-Many
One record in Table A relates to many records in Table B.
- Example: One movie has many gross income entries

### Many-to-Many
Records in Table A relate to many in Table B and vice versa.
- Requires a junction table
- Example: Actors and movies

### One-to-One
One record in Table A relates to exactly one record in Table B.
- Example: A movie and its loan

---

## Common Data Types

- CHAR(size): Fixed-length string
- VARCHAR(size): Variable-length string
- TEXT: Long-form text
- INT: Integer numbers
- DECIMAL: Exact decimal numbers
- FLOAT: Floating-point numbers
- DATETIME: Date and time values

---

## Why This Matters
Relational databases spread data across tables to reduce redundancy.  
Understanding schemas, keys, relationships, and data types is essential for:

- Writing effective SQL queries
- Combining data from multiple tables
- Maintaining data consistency and integrity

---

# SQL JOIN Operations

## Introduction to JOINs
Relational databases store data across multiple interrelated tables.

JOIN operations allow retrieval of data from multiple tables simultaneously.

Tables are linked using primary and foreign keys (though any columns with matching data types can be used).

---

## Basic JOIN Syntax

Example:

    SELECT table1.column1, table2.column2
    FROM table1
    JOIN table2
    ON table1.matching_column = table2.matching_column;

AS creates aliases for table names.  
ON clause specifies join conditions.

---

## Types of JOINs

### INNER JOIN
Returns only records with matching values in both tables.
- Default behavior of JOIN
- Equivalent to the intersection in a Venn diagram

### LEFT JOIN (LEFT OUTER JOIN)
Returns all records from the left table.
Returns matched records from the right table.
NULL values for non-matching right table records.

### RIGHT JOIN (RIGHT OUTER JOIN)
Returns all records from the right table.
Returns matched records from the left table.
NULL values for non-matching left table records.

### FULL OUTER JOIN
Returns all records from both tables.
NULL values where no matches exist.

---

## NATURAL JOIN
Automatically joins tables on columns with identical names and data types.
Produces the same result as INNER JOIN but excludes duplicate columns.

Important caveats:
- Can produce incorrect results if columns with the same name are unrelated
- Common fields like modification_date can interfere
- Safer to use INNER JOIN with explicit ON conditions

---

## Multiple Join Conditions
Required when composite keys are used.

Example:

    ON gi.movieId = gic.movieId
    AND gi.year = gic.year
    AND gi.month = gic.month

---

## Joining More Than Two Tables

Example:

    SELECT m.title, m.year, gi.year, gi.month, gic.country, gic.amount
    FROM Gross_Income AS gi
    JOIN Movie AS m ON m.movieId = gi.movieId
    JOIN Gross_Income_Country AS gic
      ON gi.movieId = gic.movieId
     AND gi.year = gic.year
     AND gi.month = gic.month;

---

## Non-Key JOINs
JOINs can use any columns with compatible data types, not just primary/foreign keys.

Example:
- Joining Person.date_birth with Review.date

---

## Summary of JOINS
Venn diagrams are commonly used:

- INNER JOIN: intersection only
- LEFT JOIN: entire left table plus intersection
- RIGHT JOIN: entire right table plus intersection
- FULL OUTER JOIN: both tables entirely

---

## Important Notes
- JOIN defaults to INNER JOIN
- Always verify column relationships when using NATURAL JOIN
- Table aliases improve readability
- Indexed join columns improve performance
- Mismatched data types cause join failures

---

# SQL & NoSQL Database Systems

## Importance of This Knowledge
Understanding database paradigms is critical because:

- Database choice impacts performance and scalability
- Most modern systems use both SQL and NoSQL
- System architecture depends heavily on database design

---

## SQL Data Manipulation Language (DML)

Purpose:
Manages data within existing database structures.

Core Commands:
- INSERT: Adds new rows
- UPDATE: Modifies existing rows
- DELETE: Removes rows
- LOCK: Controls concurrent access

Dependency:
Tables must exist (created via DDL).

---

## SQL Data Definition Language (DDL)

Purpose:
Defines and modifies database structure.

Core Commands:
- CREATE
- ALTER
- DROP
- DESCRIBE

Example:

    CREATE TABLE movie (
      movieId INT PRIMARY KEY,
      title TEXT NOT NULL
    );

---

# The Need for NoSQL & Distributed Systems

Key Points:
- Traditional RDBMS struggle with massive data volumes
- Distributed systems break data across machines
- Horizontal scaling replaces vertical scaling
- Flexible schemas support unstructured data

---

## Types of NoSQL Databases

### A. Key-Value Stores
Structure: Simple key-value pairs
Strength: Extremely fast
Weakness: Limited queries
Use cases: Caching, sessions, shopping carts
Examples: Redis, DynamoDB

### B. Document Databases
Structure: JSON or XML documents
Strength: Flexible schema
Weakness: Weak relationships
Use cases: Content management, user profiles
Examples: MongoDB, Couchbase

### C. Graph Databases
Structure: Nodes and relationships
Strength: Excellent for connected data
Weakness: Poor for tabular data
Use cases: Social networks, recommendations
Examples: Neo4j, Amazon Neptune

### D. Wide Column Stores
Structure: Sparse, wide tables
Strength: Handles massive datasets
Weakness: Complex querying
Use cases: Analytics, time-series data
Examples: Cassandra, HBase

---

## NoSQL vs Relational Databases

NoSQL Advantages:
- Horizontal scalability
- Schema flexibility
- Optimized performance
- Big data ready

Relational Strengths:
- ACID compliance
- Strong consistency
- Mature tooling
- Built-in relationships

---

## Decision Framework

Choose Relational When:
- Data is structured
- Relationships matter
- Complex joins are required
- Consistency is critical

Choose NoSQL When:
- Data is massive or unstructured
- Horizontal scalability is required
- Schema evolves frequently
- Performance depends on access patterns

---

## Real-World Application
Modern systems use multiple databases:

- Relational: Transactions and financial data
- Document: Content and catalogs
- Key-Value: Caching and sessions
- Graph: Social features and recommendations
- Wide Column: Analytics and metrics

---

## Bottom Line
Mastering SQL and NoSQL databases is essential for designing systems that are scalable, maintainable, and cost-effective in today’s data-intensive world
