# Module 3 – Data Preparation and Understanding

## Selecting Relevant Data

**Core Concept:** Choosing the right data is critical to answering your business question effectively.

### Key Principles
- **Focus on Relevance:** Only use data directly related to your analysis goal.
- **Ensure Validity & Reliability:** Crucial for trustworthy results.
- **Data Sourcing Challenges:** Needed data may not be readily available, requiring:
  - New data collection procedures.
  - Combining data from multiple sources.

### Example: Movie Viability Analysis
An entertainment producer would gather:
- Book sales (for adaptations)
- Profitability of similar movies
- Actor/location popularity in successful films

### Key Selection Questions
1. What specific data points are necessary?
2. Do I already have access, or must I find it externally?
3. Where are reliable and verifiable sources?
4. How often is the data updated?
5. What are the licensing terms and costs?
6. Is the data in a usable format, or can it be converted?

### Static and Streaming Data
Analysts work with two primary types based on when data is processed:

| Type | Description | Example |
|------|-------------|---------|
| **Static Data** | Data received and stored *prior* to analysis | Storing a week's worth of movie reviews for analysis at the end of the week |
| **Streaming Data** | Data processed and analyzed *as it is received* | Analyzing each movie review as it's posted to categorize sentiment instantly |

*Output of streaming data:* Often displayed on live dashboards or used to trigger automated functions.

---

## Data Types and Formats

### Why It Matters
Data preparation can consume **50–80%** of analysis time due to incompatibilities and necessary conversions.

### Key Challenges
1. **Format Variability:** The same type of data can appear differently.  
   *Example:* "airplane" (US) vs. "aeroplane" (UK)
2. **Time/Date Inconsistency:** Must be standardized for analysis.  
   *Examples:* DD/MM/YYYY vs. MM/DD/YYYY; 12-hour vs. 24-hour time.

### Common Time & Date Formats
- **ISO 8601:** `YYYY-MM-DDThh:mm:ss` (e.g., `2023-01-20T15:20:09`)
- **RFC 1123:** `DAY DD-MON-YYYY hh:mm:ss GMT` (e.g., `Fri 20 Jan 2023 20:20:27 GMT`)
- **American:** `MM/DD/YYYY hh:mm:ss AM/PM` (e.g., `01/20/2023 3:20:09 PM`)

### Common Data Types
| Data Type | Description & Key Use |
|-----------|-----------------------|
| **String** | Text data (letters, symbols, non-computational numbers) |
| **Integer** | Whole numbers (may include negatives); used for ordering/ranking |
| **Floating Point** | Numbers with decimal places; used in statistical analysis |
| **Date and Time** | Records when an observation was made; **formats vary widely** |
| **Boolean** | Represents **True** or **False** values (not text strings) |

**Crucial Takeaway:** Understanding and standardizing **data types and formats** is essential before performing any calculations or comparisons.

---

## Characteristics of Structured Data

Structured data refers to data that is **entered** and **maintained** in defined fields within a file or record. Structured data is easily entered, **classified**, **queried**, and **analyzed** by a computer.

This includes data found in **relational databases** and **spreadsheets**. For example, when you submit your name, address, and billing information to a website, you are creating structured data. The database may force you to enter it in a certain format for a computer to interpret it easily.

### Characteristics of Structured Data
- There is a well-defined and organized structure
- It can be stored in tables, usually within vertical columns and horizontal rows
- The content and format of the data is documented
- It is organized into files, records, and fields
- It can be searched, sorted, and queried
- Input controls can reduce the possibility of invalid data

---

## CSV Files

Different applications create files in different formats that are **not necessarily** compatible with one another. For this reason, a universal file format is needed.

Comma-separated values (CSV) files are a type of plain text file format that **is widely used to standardize data**. CSV files use commas, or other characters such as tabs, spaces, or colons, to separate columns in a table of data, and the newline character to separate rows.

Each row can also be referred to as a record. CSV files are commonly used for **importing** and **exporting** data to spreadsheets and traditional databases but can also be used as input for analytic programs and visualization tools.

---

## JSON and XML

**JSON** (JavaScript Object Notation) and **XML** (Extensible Markup Language) are also common, standardized plain text file types often used for representing data records.

- **JSON:** A lightweight data-interchange format that is easy for humans to read and write
- **XML:** A markup language that is similar to HTML

These file formats are compatible with a wide range of applications. Converting data into a common format is a valuable way to combine data from different sources.

---

## Structured File Types

There are many different types of structured data files that can either be created by humans or machine-generated:

### 1. Relational Databases
A relational database is a collection of tables with columns and rows that are connected by pre-defined relationships. Each column holds a certain kind of data, and each field stores the actual value of an attribute.

### 2. Logs
Log files are a machine-generated historical record of everything and anything that happens within a system, such as transactions, errors, or intrusions. Log files are usually considered structured data because they adhere to a standard format.

### 3. Spreadsheets
A spreadsheet file is an example of a flat file database. A flat file database stores records in a single file with no hierarchical structure. Spreadsheets are organized similarly to tables in a database, with data in rows and columns.

### 4. Sensor Readings
Sensor output is usually collected in a standardized format, which may vary by manufacturer. Individual readings may be separated only by a delimiter or may be time dependent (e.g., 1 output per second, separated by timestamps).

### 5. Transactional Records
Records of transactions can be stored in many different formats, depending on the type of transaction and its source. Some transactions are entered manually into forms, while others can be machine generated.

## Selecting Relevant Data
**Core Concept:** Choosing the right data is critical to answering your business question. #DataSelection #Relevance #CoreConcept

### Key Principles
- **Focus on Relevance:** Only use data directly related to your analysis. #Focus #RelevantData
- **Benchmarking:** Compare against industry standards or past performance. #Benchmarking #Comparison

---

### UnstructuredData RawData, NoSchema
**Core Definition**
- Unstructured Data: Raw data without a predefined organization or schema
- Not organized in a fixed format, making analysis challenging #AnalysisChallenge
- **Examples:** Photos, audio, video, web pages, blogs, PDFs, emails, social media content #DataExamples

---

# ExamplesOfUnstructuredData
- Photos/images #VisualData
- Audio files #AudioData
- Video content #VideoData
- Web pages & blogs #WebContent
- Books/journals/white papers #Documents
- PowerPoint presentations #Presentations
- Emails #EmailData
- Wikis & word processing docs #CollaborativeDocs
- PDF documents #PDFs
- Social media content (YouTube, Facebook, Twitter) #SocialMediaData
- RSS feeds #Feeds
- Traffic camera feeds #IoTData #SensorData

---

# ProcessingMethods #DataProcessing
### 1. NoSQL Databases & Data Lakes
- Store raw data in original format #RawStorage
- Centralized repositories for IoT, web, mobile, social media data #CentralizedRepo
- Ideal for real-time data storage #RealTimeData

### 2. Web Scraping
- Automated extraction from HTML pages #Automation
- Uses bots/crawlers to gather specific data #DataCrawlers
- Converts web data to databases/spreadsheets for analysis #DataConversion

### 3. APIs (Application Program Interfaces)
- RESTful APIs using HTTP & JSON #RESTAPI #JSON
- Standardized interfaces from large providers (Facebook, Google, Twitter) #StandardizedAPI
- Access subsets of large, constantly generated data #DataAccess

---

# ETL #ELT #DataPipeline
**ETL (Extract, Transform, Load)**
- **Extract:** Gather data from various sources (relational DBs, NoSQL, flat files, XML) #DataExtraction
- **Transform:** Prepare data before loading (convert formats, join, aggregate, clean data) #DataTransformation #DataCleaning
- **Load:** Load transformed data into database (apply schema rules, ensure data integrity) #DataLoading #DataIntegrity

**ELT (Extract, Load, Transform)**
- Load raw data first, transform later #RawFirst
- Used primarily for large unstructured datasets #BigData
- Transformation occurs during usage #OnDemandTransformation

---

# KeyInsights #DataManagement 
- Both structured & unstructured data are valuable #DataValue
- Organizations must format all data types for management & analysis #DataFormatting
- Transformation ensures data consistency & query success #DataConsistency
- Data lakes store real-time data in original formats #DataLakes
- APIs enable access to massive social media datasets #APIAccess
