### Table Name : Challan Details

Description : Use to store details of Challan.
<br><br>

**Table Creation**

```sql
CREATE TABLE challan_details (
 challan_no VARCHAR(6) REFERENCES challan_header(challan_no),
 product_no VARCHAR(6) REFERENCES product_master(product_no),
 qty_disp NUMERIC(8)
);
```


**Insertion Queries**

```sql
INSERT INTO challan_details VALUES ('CH9001','P00001',4);
INSERT INTO challan_details VALUES ('CH9001','P07965',1);
INSERT INTO challan_details VALUES ('CH9001','P07885',1);
INSERT INTO challan_details VALUES ('CH6865','P07868',3);
INSERT INTO challan_details VALUES ('CH6865','P03453',4);
INSERT INTO challan_details VALUES ('CH6865','P00001',10);
INSERT INTO challan_details VALUES ('CH3965','P00001',5);
INSERT INTO challan_details VALUES ('CH3965','P07975',2);
```

