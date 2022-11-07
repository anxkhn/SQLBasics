### Table Name : Product Master

Description : Use to store information about products.
<br><br>

**Table Creation**

```sql
CREATE TABLE product_master (
  Product_no VARCHAR(6) PRIMARY KEY, 
  Description VARCHAR(50) NOT NULL, 
  Profit_percent NUMERIC(5,2) NOT NULL, 
  Unit_measure VARCHAR(10) NOT NULL, 
  Qty_on_hand NUMERIC(8) NOT NULL, 
  Reorder_lvl NUMERIC(8) NOT NULL, 
  Sell_price NUMERIC(8,2) NOT NULL, 
  Cost_price NUMERIC(8,2) NOT NULL,
  CHECK (Product_no like 'P%'),
  CHECK (Sell_price <>0), 
  CHECK (Cost_price <>0)
);
```

_Note : Description size has been increased to 50 from 5 to store entire input. Cannot be 0 is constraint is yet to be implemented (PRs are welcomed)._

**Insertion Queries**

```sql
INSERT INTO Product_master VALUES ('P00001','1.44 Floppies',5,'Piece',100,20,525,500);
INSERT INTO Product_master VALUES ('P03453','Monitors',6,'Piece',10,3,12000,11200);
INSERT INTO Product_master VALUES ('P06734','Mouse',5,'Piece',20,5,1050,1000); 
INSERT INTO Product_master VALUES ('P07865','1.22 Floppies',5,'Piece',100,20,525,500);
INSERT INTO Product_master VALUES ('P07868','Keyboards',2,'Piece',10,3,3150,3050); 
INSERT INTO Product_master VALUES ('P07885','CD Drive',2.5,'Piece',10,3,5250,5100);
INSERT INTO Product_master VALUES ('P07965','540 HDD',4,'Piece',10,3,8400,8000); 
INSERT INTO Product_master VALUES ('P07975','1.44 Drive',5,'Piece',10,3,1050,1000);
INSERT INTO Product_master VALUES ('P08865','1.22 Drive',5,'Piece',2,3,1050,1000);
```
