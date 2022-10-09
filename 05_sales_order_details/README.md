### Table Name : Sales Order Details

**Table Creation**

```sql
create table sales_order_details
(
 s_order_no varchar(6) references sales_order(s_order_no),
 product_no varchar(6) references product_master(product_no),
 qty_ordered numeric(8),
 qty_disp numeric(8),
 product_rate numeric(10,2)
);
```

**Insertion Queries**

```sql
INSERT INTO sales_order_details VALUES ('O19001','P00001',4,4,525);  
INSERT INTO sales_order_details VALUES ('O19001','P07965',2,1,8400);  
INSERT INTO sales_order_details VALUES ('O19001','P07885',2,1,5250);  
INSERT INTO sales_order_details VALUES ('O19002','P00001',10,0,525);  
INSERT INTO sales_order_details VALUES ('O46865','P07868',3,3,3150);  
INSERT INTO sales_order_details VALUES ('O46865','P07885',3,1,5250);  
INSERT INTO sales_order_details VALUES ('O46865','P00001',10,10,525);  
INSERT INTO sales_order_details VALUES ('O46865','P03453',4,4,1050);  
INSERT INTO sales_order_details VALUES ('O19001','P03453',2,2,1050);  
INSERT INTO sales_order_details VALUES ('O19001','P06734',1,1,12000);  
INSERT INTO sales_order_details VALUES ('O19001','P07965',1,0,8400);  
INSERT INTO sales_order_details VALUES ('O19001','P07975',1,0,1050);  
INSERT INTO sales_order_details VALUES ('O19001','P00001',10,5,525);  
INSERT INTO sales_order_details VALUES ('O19001','P07975',5,3,1050);
```