## 1.1 Optimistic

- Multiple transactions or users are allowed to access a resource.
    
- It’s assumed conflicts will rarely occur.
    
- Conflicts are only checked during the **commit** stage.
    
- During a conflict, the system checks if the data has been modified by another process.  
    If yes — a **conflict exception** is thrown, and the user needs to **retry or resolve** the conflict.
    

## 1.2 Pessimistic

- It’s assumed conflicts will likely occur.
    
- When a resource is accessed, a **lock** is placed on it.
    

Example SQL:

sql

`-- Lock the row with an update lock to prevent other transactions from modifying  SELECT * FROM employees WITH (UPDLOCK) WHERE employee_id = 123; -- Perform the update on the locked row UPDATE employees SET salary = salary * 1.05 WHERE employee_id = 123; -- Commit the transaction to release the lock COMMIT;`