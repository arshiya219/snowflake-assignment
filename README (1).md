# Snowflake Tutorial Assignment

## Overview

This repository contains the implementation and practical demonstration
of a Snowflake Tutorial Assignment using Snowflake SQL Worksheets and
Snowflake Notebooks.

The assignment covers:

1.  SnowSQL Login and Connection
2.  Creation of Snowflake Objects
3.  Data Loading Using SnowSQL
4.  Snowflake Time Travel
5.  Data Recovery Using Time Travel

## Tools and Technologies

-   Snowflake
-   Snowflake SQL Worksheets
-   Snowflake Notebooks
-   SQL
-   SnowSQL concepts
-   Snowflake Time Travel

## Assignment Structure

``` text
snowflake-assignment/
│
├── question1.sql
├── question2.sql
├── Q3.ipynb
├── Q4.ipynb
├── Q5.ipynb
├── README.md
│
└── screenshots/
    ├── question1.png
    ├── question2.png
    ├── question2_objects.png
    ├── question3.png
    ├── question4.png
    └── question5.png
```

## Question 1 -- SnowSQL Login and Connection

The Snowflake environment was accessed successfully and the connection
was verified using SQL functions.

The following details were displayed:

-   Current User
-   Current Role
-   Current Warehouse
-   Current Database
-   Current Schema

SQL functions used include:

``` sql
SELECT
    CURRENT_USER() AS CURRENT_USER,
    CURRENT_ROLE() AS CURRENT_ROLE,
    CURRENT_WAREHOUSE() AS CURRENT_WAREHOUSE,
    CURRENT_DATABASE() AS CURRENT_DATABASE,
    CURRENT_SCHEMA() AS CURRENT_SCHEMA;
```

### Output

![Question 1 Output](screenshots/question1.png)

------------------------------------------------------------------------

## Question 2 -- Creation of Snowflake Objects

The following Snowflake objects and operations were demonstrated:

-   Database
-   Schema
-   Warehouse
-   Table
-   Stage
-   INSERT operation
-   SELECT operation
-   UPDATE operation
-   DELETE operation

A sample `STUDENTS` table was created with the following attributes:

-   `STUDENT_ID`
-   `STUDENT_NAME`
-   `DEPARTMENT`
-   `MARKS`

Sample student records were inserted and basic DML operations were
performed.

### Snowflake Objects

![Question 2 Objects](screenshots/question2.png)

### Table / SQL Execution

![Question 2 Table](screenshots/question2_objects.png)

------------------------------------------------------------------------

## Question 3 -- Data Loading Using SnowSQL

A sample employee CSV dataset was created and loaded into Snowflake
using the Snowflake data-loading process based on the `PUT` and
`COPY INTO` pattern.

The process included:

1.  Creating sample CSV data
2.  Creating an employee table
3.  Creating an internal stage
4.  Uploading the CSV file to the stage
5.  Listing staged files
6.  Loading data using `COPY INTO`
7.  Verifying the loaded records

### Output

![Question 3 Output](screenshots/question3.png)

------------------------------------------------------------------------

## Question 4 -- Snowflake Time Travel

Snowflake Time Travel was demonstrated using an `ORDERS` table.

The demonstration included:

1.  Creating the table
2.  Inserting sample records
3.  Viewing the original data
4.  Capturing a reference timestamp
5.  Performing an UPDATE operation
6.  Performing a DELETE operation
7.  Viewing the modified data
8.  Querying an earlier version using Time Travel

Time Travel syntax was demonstrated using historical queries such as:

``` sql
SELECT *
FROM ORDERS
AT (OFFSET => -5);
```

### Output

![Question 4 Time Travel Output](screenshots/question4.png)

------------------------------------------------------------------------

## Question 5 -- Data Recovery Using Time Travel

Snowflake Time Travel was used to demonstrate recovery of records that
were accidentally deleted.

The process included:

1.  Creating a product inventory table
2.  Inserting sample records
3.  Viewing the original data
4.  Capturing a snapshot/reference time
5.  Simulating accidental deletion
6.  Viewing the data after deletion
7.  Identifying deleted records using Time Travel
8.  Recovering the deleted records
9.  Verifying the recovered data

### Output

![Question 5 Recovery Output](screenshots/question5.png)

------------------------------------------------------------------------

## Conclusion

The assignment demonstrates the basic use of Snowflake for database and
schema management, table creation, data manipulation, data loading,
historical data access, and recovery using Time Travel.

All practical demonstrations were performed in the Snowflake environment
and the corresponding SQL files/notebooks and screenshots are included
in this repository.

## Author

**Arshiya Shaik**
