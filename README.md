# SQLBasics
A repo for basic SQL Commands,
intended for personal use.

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


### Show Table (query)
```sql
SELECT * FROM table_name;
```

### Drop Databases

```sql
DROP DATABASE database_name;
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

### Drop Table

```sql
DROP TABLE table_name;
```

### Alter Table (Add Column)

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

### Alter Table (Drop Column)

```sql
DROP DATABASE database_name;
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


### Constrains

```sql
CREATE TABLE Persons (
    ID int PRIMARY,
    FirstName varchar(255) NOT NULL,
    AadharNo int UNIQUE,
    City varchar(255) DEFAULT 'Mumbai',
    Personid int IDENTITY(1,1)
    Age int,
    CHECK (Age>=18)
);
```

### Constrains - Foreign Key

```sql
CREATE TABLE Orders (
    OrderID int PRIMARY,
    OrderNumber int NOT NULL,
    ID int,
    FOREIGN KEY (ID) REFERENCES Persons(ID)
);
```

