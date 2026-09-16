# snowflake-assignment
Snowflake Tutorial Assignment demonstrating Snowflake SQL, database and schema creation, data loading, DML operations, Time Travel, and data recovery.
Snowflake Tutorial Assignment

Overview

This repository contains the implementation and practical demonstration
of a Snowflake Tutorial Assignment using Snowflake SQL Worksheets and
Snowflake Notebooks.

The assignment covers:

SnowSQL Login and Connection

Creation of Snowflake Objects

Data Loading Using SnowSQL

Snowflake Time Travel

Data Recovery Using Time Travel

Tools and Technologies

Snowflake

Snowflake SQL Worksheets

Snowflake Notebooks

SQL

SnowSQL concepts

Snowflake Time Travel

Assignment Structure

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

Question 1 -- SnowSQL Login and Connection

The Snowflake environment was accessed successfully and the connection
was verified using SQL functions.

The following details were displayed:

Current User

Current Role

Current Warehouse

Current Database

Current Schema

SQL functions used include:

SELECT
    CURRENT_USER() AS CURRENT_USER,
    CURRENT_ROLE() AS CURRENT_ROLE,
    CURRENT_WAREHOUSE() AS CURRENT_WAREHOUSE,
    CURRENT_DATABASE() AS CURRENT_DATABASE,
    CURRENT_SCHEMA() AS CURRENT_SCHEMA;

Output



Question 2 -- Creation of Snowflake Objects

The following Snowflake objects and operations were demonstrated:

Database

Schema

Warehouse

Table

Stage

INSERT operation

SELECT operation

UPDATE operation

DELETE operation

A sample STUDENTS table was created with the following attributes:

STUDENT_ID

STUDENT_NAME

DEPARTMENT

MARKS

Sample student records were inserted and basic DML operations were
performed.

Snowflake Objects



Table / SQL Execution



Question 3 -- Data Loading Using SnowSQL

A sample employee CSV dataset was created and loaded into Snowflake
using the Snowflake data-loading process based on the PUT and
COPY INTO pattern.

The process included:

Creating sample CSV data

Creating an employee table

Creating an internal stage

Uploading the CSV file to the stage

Listing staged files

Loading data using COPY INTO

Verifying the loaded records

Output



Question 4 -- Snowflake Time Travel

Snowflake Time Travel was demonstrated using an ORDERS table.

The demonstration included:

Creating the table

Inserting sample records

Viewing the original data

Capturing a reference timestamp

Performing an UPDATE operation

Performing a DELETE operation

Viewing the modified data

Querying an earlier version using Time Travel

Time Travel syntax was demonstrated using historical queries such as:

SELECT *
FROM ORDERS
AT (OFFSET => -5);

Output



Question 5 -- Data Recovery Using Time Travel

Snowflake Time Travel was used to demonstrate recovery of records that
were accidentally deleted.

The process included:

Creating a product inventory table

Inserting sample records

Viewing the original data

Capturing a snapshot/reference time

Simulating accidental deletion

Viewing the data after deletion

Identifying deleted records using Time Travel

Recovering the deleted records

Verifying the recovered data

Output



Conclusion

The assignment demonstrates the basic use of Snowflake for database and
schema management, table creation, data manipulation, data loading,
historical data access, and recovery using Time Travel.

All practical demonstrations were performed in the Snowflake environment
and the corresponding SQL files/notebooks and screenshots are included
in this repository.

Author

Arshiya Shaik
