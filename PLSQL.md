### TRIGGER
A database trigger is a stored program which is automatically fired or executed when some events occur. A trigger can execute in response to any of the following events:
1. A database manipulation (DML) statement like DELETE, INSERT or UPDATE.
2. A database definition (DDL) statement like CREATE, ALTER or DROP.
3. A database operation like SERVERERROR, LOGON, LOGOFF, STARTUP, or SHUTDOWN.

```sql
CREATE [OR REPLACE] TRIGGER trigger_name
{BEFORE | AFTER | INSTEAD OF }
{INSERT [OR] | UPDATE [OR] | DELETE}
[OF col_name]
ON table_name
[REFERENCING OLD AS o NEW AS n]
[FOR EACH ROW]
WHEN (condition)
BEGIN
--- sql statements
END;
```

### CURSOR
A cursor is a pointer to context area i.e. Context area is controlled by the cursor. It is used to fetch and manipulate the data returned by the SQL statement.

#### Types of cursors:
1. Implicit cursors.
2. Explicit cursors.

### Example of implicit cursor

```sql
DECLARE  var_rows number(2);
BEGIN
  UPDATE employees 
  SET salary = salary + 2000;
  IF SQL%NOTFOUND THEN
    dbms_output.put_line('No record updated.');
  ELSIF SQL%FOUND THEN
    var_rows := SQL%ROWCOUNT;
    dbms_output.put_line(var_rows || ' records are updated.');
  END IF; 
END;
```

### Example of explicit cursor

```sql
DECLARE
   s_rollNo students.rollNo%type;
   s_name students.name%type;
   s_address students.address%type;
   CURSOR cur_students is
      SELECT rollNo, name, address FROM students;
BEGIN
   OPEN cur_students;
   LOOP
      FETCH cur_students into s_rollNo, s_name, s_address;
      EXIT WHEN cur_students%notfound;
      dbms_output.put_line(s_rollNo || ' ' || s_name || ' ' || s_address);
   END LOOP;
   CLOSE cur_students;
END;
```
