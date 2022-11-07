### Table Name : Salesman Master

Description : Use to store information about salesman working in the company.
<br><br>

**Table Creation**

```sql
CREATE TABLE salesman_master (
  Salesman_no VARCHAR(6) PRIMARY KEY, 
  Salesman_name VARCHAR(20) NOT NULL, 
  Address1 VARCHAR(30) NOT NULL, 
  Address2 VARCHAR(30), 
  City VARCHAR(20), 
  PinCode VARCHAR(6), 
  State VARCHAR(20), 
  Sal_amt NUMERIC(8,2) NOT NULL, 
  Tgt_to_get NUMERIC(6,2) NOT NULL, 
  Ytd_sales NUMERIC(6,2) NOT NULL, 
  Remarks VARCHAR(60), 
  CHECK (Salesman_no LIKE 'S%'),
  CHECK (Sal_amt <>0),
  CHECK (Tgt_to_get <>0)
);
```


**Insertion Queries**

```sql
INSERT INTO salesman_master VALUES ('S00001','Kiran','A/14','Worli','Bombay','400002','Maharashtra',3000,100,50,'Good');  
INSERT INTO salesman_master VALUES ('S00002','Manish','65','Nariman','Bombay','400001','Maharashtra',3000,200,100,'Good');     
INSERT INTO salesman_master VALUES ('S00003','Ravi','P-7','Bandra','Bombay','400032','Maharashtra',3000,200,100,'Good');        
INSERT INTO salesman_master VALUES ('S00004','Ashish','A/5','Juhu','Bombay','400044','Maharashtra',3000,200,150,'Good');             
```
