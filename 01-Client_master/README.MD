### Table Name : Client Master

Description : Use to store information about clients.
<br><br>

**Table Creation**

```sql
CREATE TABLE Client_master (
  Client_no varchar(6) PRIMARY KEY, 
  Name varchar(25) NOT NULL, 
  Address1 varchar(20), 
  Address2 varchar(20), 
  City varchar(15), 
  Pincode numeric(8), 
  State varchar(15), 
  Bal_due numeric(10, 2),
  CHECK (Client_no like 'C%')
);
```

_Note : The order is City, Pincode and State._

**Insertion Queries**

```sql
INSERT INTO Client_master VALUES ('C001','Ivan Bayross',' ',' ','Bombay',400054,'Maharashtra', 15000);
INSERT INTO Client_master VALUES ('C002','Vandana Saitwal',' ',' ','Madras',780001, 'Tamil Nadu',0);
INSERT INTO Client_master VALUES ('C003','Pramada Jaguste', ' ', ' ', 'Bombay', 400057, 'Maharashtra', 5000);
INSERT INTO Client_master VALUES ('C004','Basu Navindgi', ' ', ' ', 'Bombay', 400056, 'Maharashtra',0);
INSERT INTO Client_master VALUES ('C005','Ravi Sreedharam',' ', ' ', 'Delhi', 110001, ' ',2000);
INSERT INTO Client_master VALUES ('C006','Rukmini',' ', ' ', 'Bombay', 400050, 'Maharashtra',0);
```
