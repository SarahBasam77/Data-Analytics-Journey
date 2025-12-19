# Part 1: Flat File Databases
## What is a Flat File Database?
A simple data storage method using rows (records) and columns (fields), like spreadsheets or CSV files.

## Key Characteristics:
- Easy to set up
- Good for small datasets
- Each row has the same structure

## Limitations:
- Data redundancy
- Inconsistency
- Poor scalability
- Inflexible structure

## Transition to Relational Databases:
Relational databases use multiple linked tables, reduce redundancy, and improve scalability.

# Part 2: The SQL Query Language
## What is SQL?
Structured Query Language, the standard for communicating with relational databases.

## Key Functions (CRUD):
- Create/Add
- Read/Retrieve
- Update/Modify
- Delete/Remove

## SQL Components:
### DML (Data Manipulation Language) – Work with data (SELECT, INSERT, UPDATE, DELETE)
### DDL (Data Definition Language) – Define structure (create tables, set data types)

#### Note: SQL is universal, but implementations (MySQL, PostgreSQL, etc.) may vary.

# Part 3: Using SQL to Query Data
## Core Query Structure:
SELECT columns
FROM table
WHERE conditions
ORDER BY column [ASC|DESC];

## Key Clauses:
- SELECT – Choose columns
- WHERE – Filter rows
- ORDER BY – Sort results

## SQL Operators:
### Logical: AND, OR, NOT
### Comparison: =, !=, >, <, BETWEEN, LIKE, IN

# Part 4: Using Operators in SQL Queries
## Aggregate Functions:
COUNT(), AVG(), SUM(), MAX(), MIN()

## GROUP BY Clause:
Groups rows for per-category calculations

## HAVING Clause:
Filters grouped results (similar to WHERE but for groups)

### Example Workflow:
SELECT MovieId, 
COUNT(*) AS Review_Count,
AVG(Score) AS Avg_Score
FROM Review
GROUP BY MovieId
HAVING AVG(Score) > 7.0
ORDER BY Avg_Score DESC;

# Part 5: SQL Best Practices
## 1. Keyword Capitalization
Use uppercase for SQL keywords
## 2. Proper Spacing
Separate keywords from variables
## 3. String Formatting
Use single quotes for text
## 4. Aliases for Clarity
Use AS for meaningful column names
## 5. Structural Formatting
Place clauses on separate lines, use indentation
## 6. Comments for Documentation
Use -- for notes
## 7. Organizational Standards
Follow team/style guides


# Quick Reference Table: SQL Concepts
Concept	Purpose	Key Syntax	
## Example
### SELECT	Retrieve data
SELECT col FROM table	
SELECT title FROM Movie

### WHERE	Filter rows	
WHERE condition	
WHERE year > 1976

### ORDER BY	Sort results	
ORDER BY col DIR	
ORDER BY title ASC

### Aggregates 
Calculate stats
FUNC(col)	
AVG(Score)
COUNT(*)

### GROUP BY	
Group rows	
GROUP BY col	
GROUP BY MovieId

### HAVING Filter groups
HAVING condition	
HAVING AVG(Score) > 7.0

### Aliases	Rename 
columns	col AS alias	
COUNT(*) AS Total

### Comments	Documentation	
-- comment	-- Get top 10 movies

#### Key Takeaways
- Flat files are simple but limited.
- Relational databases organize data efficiently across linked tables.
- SQL provides standardized access to database operations.
- Query clauses enable precise data retrieval.
- Aggregate functions perform calculations in-database.
- GROUP BY and HAVING enable group-level analysis.

Best practices ensure readable and maintainable SQL code.

Always consider specific RDBS variations in syntax and features.

Evolutionary Perspective:
Flat files → Relational databases → SQL → Advanced queries → Professional practices
This approach enables efficient data management from simple storage to complex analysis while maintaining integrity and standards.
