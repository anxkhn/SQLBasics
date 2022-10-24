# Basic SQL Queries

## Display entire table content
```sql
SELECT * FROM client_master;
```

## Display client names 
```sql
SELECT name FROM client_master;
``` 

## Display client names and city
```sql
SELECT name,city FROM client_master;
```

## Display client names, city and arrange client names in alphabetical order
```sql
SELECT name , city FROM client_master 
ORDER BY name;
```

## Display client no and bal_due and arrange bal_due in decreasing/descending order
```sql
SELECT client_no,bal_due FROM client_master 
ORDER BY client_no desc ;
```

## Display names starting from 'R'
```sql
SELECT name FROM client_master
WHERE name LIKE 'R%';
```
> Note: 'r%' is not case sensitive.

## Display names having  'A' as the second alphabet 
```sql
SELECT name FROM client_master
WHERE name LIKE '_A%';
```

## Display names,city of clients living in Bombay or Delhi
```sql
SELECT name , city FROM client_master
WHERE city='Bombay' OR city='Delhi';
```

## Display client name whose balance due is greater than 10000 
```sql
SELECT name, bal_due FROM client_master
WHERE bal_due>10000;
```
## Display order info of orders placed in January
```sql
SELECT s_order_no,s_order_date FROM sales_order
WHERE s_order_date  LIKE '__%01%'; 
```
