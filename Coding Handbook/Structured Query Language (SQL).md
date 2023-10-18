#### Introduction

Structured Query Language (SQL) is a **domain-specific** language designed to manage data in a relational database system.

There are many different databases built on SQL, with the more popular ones being MySQL, MongoDB, and MariaDB.

##### Basic Concepts

The basic concepts of all SQL database management systems are **databases**, **tables**, and **entries** (rows).

A database is a **container** that can hold **multiple** tables along with the data dictionary and metadata describing those tables. It serves as an **organizational unit** (OU) for managing and storing data.

A table is a structure within a database that is used to organize data into **rows** and **columns**. Each column has a set **data type** that entries must comply to, while each row represents a **table entry**.

Each entry in a table represents a record. The **uniqueness** of each record is **dependent** on the **primary key**, which will be covered later.

##### Data Types

Similar to programming languages, SQL has data types that are set in each column, defining what values are able to be placed in that specific column. For SQL, each data 

The most common data types are:
 - **VARCHAR(n)** - Similar to a string, this allows you to input a text string containing **letters**, **numbers**, and **special characters**, up to the maximum of `n` bytes. 
 - **INT/INTEGER** - A **16-bit (medium)** integer allowing the default range of a **signed** integer to be **-2,147,483,648** to **2,147,483,647**. However, there exists an **unsigned** integer, which is an integer that only accepts positive values, giving a bigger positive range of **0** to **4,294,967,295** to work with.
 - **FLOAT** - A float is a **32-bit** floating-point (decimal) value that goes from the range `-3.4 × 10^38` to `3.4 × 10^38`, with up to about **7** digits of precision.
 - **DOUBLE** - A double is a **64-bit** version of a float, giving up to **15** digits of precision and a range of about `-1.8 × 10^308` to `1.8 × 10^308`.
 - **BOOL/BOOLEAN** - Used to store either **True** or **False**, but can also store **zero values** as false and **nonzero values** as true.
 - **DATETIME**
 - **DATE**
 - **TIME**
 - **YEAR**

##### The Database

The metadata of the database contains the **name** of the database, the **name** and **structure** of each table within the database, **created users and their permissions** in the database, as well as **additional database parameters** that are created by the database engine (MySQL, MariaDB, etc.).

To access the database, you require its **login details**, which typically include:
 - Database IP Address
 - Database Port (default: 3306)
 - Database Name
 - Username (default: root)
 - Password

##### Commands



##### Constraints (PRIMARY_KEY, AUTO_INCREMENT)