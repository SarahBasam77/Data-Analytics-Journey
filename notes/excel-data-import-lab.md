# Lab Summary: Basic Excel Concepts & Data Import

## Table of Contents
1. [Basic Excel Concepts Lab](#basic-excel-concepts-lab)
2. [Importing Data into Excel Lab](#importing-data-into-excel-lab)
3. [Combined Practical Applications](#combined-practical-applications)
4. [Quick Reference Cheatsheet](#quick-reference-cheatsheet)

---

## Basic Excel Concepts Lab

### Objectives
- Perform basic Excel functions
- Learn formulas and functions
- Practice number formatting

### Part 1: Basic Excel Formulas

#### Key Concepts
## - Formulas begin with `=` sign Can be typed directly in cells or formula bar
## - Basic operations: `+`, `-`, `*`, `/`

#### Exercises Completed
## 1. Created simple calculations:
## `=1+1` in cell A1
   - `=4-2` in cell A2
   - `=2*4` in cell A3
   - `=6/2` in cell A4

2. Used cell references:
   - Values in A1, B1 with formula `=A1+B1` in C1
   - Formulas automatically adjust when rows/columns are added

3. Built comprehensive operations table:
   - Added descriptive column A
   - Inserted header row
   - Formulas remained functional after modifications

### Part 2: Basic Excel Functions

#### Functions Used
1. **SUM**: `=SUM(A1:A5)` - Adds range of cells
2. **AVERAGE**: `=AVERAGE(B2:B6)` - Calculates mean
3. **COUNT**: `=COUNT(C2:C6)` - Counts number of cells
4. **MIN**: `=MIN(D2:D6)` - Returns smallest value
5. **MAX**: `=MAX(E2:E6)` - Returns largest value

#### Observations
- Excel suggests cell ranges automatically
- Functions use colon (`:`) for ranges (more efficient than individual cell references)
- Formulas update when source data changes

### Part 3: Formatting & Worksheet Management

#### Techniques Learned
- **Inserting Rows/Columns**: Right-click → Insert
- **Column Width Adjustment**: Drag border between column headers
- **Text Formatting**: `CTRL+B` for bold
- **Worksheet Renaming**: Right-click sheet tab → Rename
- **Data Organization**: Created "Formulas" and "Functions" worksheets

---

## Importing Data into Excel Lab

### Lab Overview
**Title**: Lab - Importing Data into Excel  
**Objective**: Learn how to review, prepare, and import data files into Excel with focus on delimiter fields and CSV format.

### Key Learning Objectives
- Review delimited text files and save them as CSV files
- Open CSV files using the free version of Excel
- Import text and CSV files using the full version of Excel

### Part 1: Review a Delimited Text File and Save as CSV

#### Step 1: Review text file in text editor
- Downloaded "bike sales.txt" file
- Opened in Notepad/text editor to examine structure

**Key observations**:
- First line contains header information
- Contains 13 data columns
- Uses comma (,) as delimiter to separate data
- Headers: Date, Month, Year, Customer_Age, Age_Group, Gender, Country, State, Product_Category, Order_Quantity, Profit, Cost, Revenue

#### Step 2: Save as CSV file
- Saved "bike sales.txt" as "bike sales.csv"
- Uploaded CSV to OneDrive (for free Excel version)

### Part 2: Opening CSV with Free Excel Version
**Limitations**: Free Excel lacks automatic import features for delimited text  
**Process**: File → Open → View more files → Select bike sales.csv  
**Note**: Excel automatically converts to .xlsx format when opened

### Part 3: Importing Files in Full Excel Version
**Step 1: Import data file**
- Start Excel → Data → Get Data → From File → From Text/CSV
- Open "bike sales.txt"
- **Key feature**: Excel automatically recognizes comma delimiters and columns
- Load data: Creates organized table in worksheet

### Important Concepts

#### CSV Format
- **What**: Comma Separated Values - text-only format readable by many programs
- **Why**: Common format for data transmission and import/export
- **Structure**: Each data field separated by commas, each record on new line

#### Delimiters
- **Definition**: Characters that separate data fields
- **Most common**: Commas (,) in CSV files
- **Other delimiters**: Tabs, semicolons, pipes (|)
- **Importance**: Excel uses delimiters to recognize and separate data into columns

#### Version Differences
- **Free Excel (Office.com)**: Requires CSV format, can't import delimited text directly
- **Full Excel**: Has advanced import tools (Get Data feature), can handle various formats

### Practical Skills Gained
- File conversion: Text → CSV format
- Data inspection: Understanding file structure before import
- Import techniques: Different approaches for different Excel versions
- Troubleshooting: Recognizing delimiter issues and format requirements

---

## Combined Practical Applications

### Complete Data Workflow Example
1. Data Collection → "bike sales.txt" (raw data)
2. Preparation → Convert to CSV format
3. Import → Excel (using appropriate method)
4. Analysis → Apply formulas/functions learned in first lab
5. Formatting → Organize and present data professionally

### Real-World Use Cases
1. **Business Reports**: Import sales data → Calculate totals → Format for presentation
2. **Data Analysis**: Import raw data → Clean with formulas → Analyze trends
3. **Academic Research**: Import survey data → Calculate statistics → Create visualizations
4. **Personal Finance**: Import bank statements → Categorize expenses → Calculate budgets

### Best Practices
1. **Before Import**: Always inspect raw data files to understand structure
2. **During Import**: Verify delimiter recognition and column alignment
3. **After Import**: Check for data integrity and formatting consistency
4. **Documentation**: Note source, date, and any transformations applied


## Quick Reference Cheatsheet
### Excel Formulas & Functions
```excel
Basic Operations:
=1+1    # Addition
=4-2    # Subtraction
=2*4    # Multiplication
=6/2    # Division

Common Functions:
=SUM(A1:A5)          # Sum of range
=AVERAGE(B2:B6)      # Average of range
=COUNT(C2:C6)        # Count cells
=MIN(D2:D6)          # Minimum value
=MAX(E2:E6)          # Maximum value

Cell References:
=A1+B1              # Basic cell reference
=SUM(A10:A12)       # Range reference

Free Excel (Office.com):
1. File → Open → View more files → Select CSV
2. Automatically converts to .xlsx

Full Excel:
1. Data → Get Data → From File → From Text/CSV
2. Select delimiter type
3. Load to worksheet
