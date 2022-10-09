### Table Name : Sales Order

**Table Creation**

```sql
create table sales_order
(s_order_no varchar(6) PRIMARY KEY CHECK(s_order_no like 'O%'),
s_order_date date,
client_no varchar (6) references Client_master(client_no),
dely_add varchar(25),
salesman_no varchar(6) references salesman_master(salesman_no),
dely_type char(1) check(dely_type IN ('P','F')),
bill_yn char(1),
dely_date date,
check(dely_date > s_order_date),
order_status varchar (10) check (order_status IN ('IP','F','BO','C'))
);
```

**Insertion Queries**

```sql
insert into sales_order(s_order_no, s_order_date, client_no, dely_add, bill_yn, salesman_no, dely_date, order_status) values
('O19001', '1996-01-12', 'C00001', 'F', 'N', 'S00001', '1996-01-20', 'IP'),
('O19002', '1996-01-25', 'C00002', 'P', 'N', 'S00002', '1996-01-27', 'C'),
('O46865', '1996-02-18', 'C00003', 'F', 'Y', 'S00003', '1996-02-20', 'F'),
('O19003', '1996-04-03', 'C00001', 'F', 'Y', 'S00001', '1996-04-07', 'F'),
('O46866', '1996-05-20', 'C00004', 'P', 'N', 'S00002', '1996-05-22', 'C'),
('O10008', '1996-05-24', 'C00005', 'F', 'N', 'S00004', '1996-05-26', 'IP');
```