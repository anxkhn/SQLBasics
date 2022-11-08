# SQLBasics
A repo for basic MySQL Commands and for storing Lab Assignments.

### Show Databases

```sql
SHOW DATABASES;
```

### Create Databases

```sql
CREATE DATABASE database_name;
```

### Use Databases

```sql
USE database_name;
```


### Drop Databases

```sql
DROP DATABASE database_name;
```

### Show Tables
```sql
SHOW TABLES;
```

### Describe Table
```sql
DESCRIBE table_name
```
or
```sql
DESC table_name
```

### Show Table (query)
```sql
SELECT * FROM table_name;
```


### Create Table

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
```
### Describe Structure of a Table

```sql
DESCRIBE table_name;
```

### Drop Table

```sql
DROP TABLE table_name;
```

### Truncate Table

```sql
TRUNCATE TABLE table_name;
```

### Alter Table (Add Column)

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

### Alter Table (Drop Column)

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

### Alter Table (Modify Column)

```sql
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
```
or
```sql
ALTER TABLE table_name
ALTER COLUMN column_name datatype;
```


### Constraints

```sql
CREATE TABLE Persons (
    ID int PRIMARY KEY,
    FirstName varchar(255) NOT NULL,
    AadharNo int UNIQUE,
    City varchar(255) DEFAULT 'Mumbai',
    Personid int IDENTITY(1,1)
    Age int,
    CHECK (Age>=18)
);
```

### Constraints - Foreign Key

```sql
CREATE TABLE Orders (
    OrderID int PRIMARY KEY,
    OrderNumber int NOT NULL,
    ID int,
    FOREIGN KEY (ID) REFERENCES Persons(ID)
);
```

<br><br><br>

[Client_master](https://github.com/anxkhn/SQLBasics/tree/main/01-Client_master) <br>
[product_master](https://github.com/anxkhn/SQLBasics/tree/main/02-product_master) <br>
[salesman_master](https://github.com/anxkhn/SQLBasics/tree/main/03-salesman_master) <br>
[sales_order](https://github.com/anxkhn/SQLBasics/tree/main/04-sales_order) <br>
[sales_order_details](https://github.com/anxkhn/SQLBasics/tree/main/05_sales_order_details) <br>
[challan_header](https://github.com/anxkhn/SQLBasics/tree/main/06-challan_header) <br>
[challan_details](https://github.com/anxkhn/SQLBasics/tree/main/07-challan_details) <br><br>
[Assignment List](https://github.com/anxkhn/SQLBasics/raw/main/SQL_LAB.pdf)
<br><br>

### Feel free to refer my personal code repos. 

Create ISSUE if you find any. PULL REQUESTS are welcomed. <br>
Please use it responsibly. Thank you!
