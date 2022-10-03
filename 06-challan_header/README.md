
### Table Name : Challan Header

Description : Use to store information about challans made for the order.
<br><br>

**Table Creation**

```sql
CREATE TABLE challan_header (
 challan_no VARCHAR(6) PRIMARY KEY check(challan_no like 'CH%'),
 s_order_no VARCHAR(6) REFERENCES sales_order(s_order_no),
 challan_date DATE NOT NULL,
 billed_yn CHAR(1) 
);
```


**Insertion Queries**

```sql
INSERT INTO challan_header VALUES ('CH9001','O19001','1995-12-12','Y');
INSERT INTO challan_header VALUES ('CH6865','O46865','1995-11-12','Y');
INSERT INTO challan_header VALUES ('CH3965','O10008','1995-10-12','Y');
```
