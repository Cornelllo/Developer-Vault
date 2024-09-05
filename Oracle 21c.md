How to unlock and change password of a user in windows OS.
**Open command prompt or any terminal and execute:**
    
    sqlplus / as sysdba
    
 **To get the database name:**
    
    `SELECT NAME FROM V$DATABASE;`
    
This query will return the name of the current database you are connected to.

**To list all available services:**
    
    `SELECT NAME FROM V$SERVICES;`
    
This query will show all services registered with the listener, including the default database service and any additional services configured.

**Once identified connect to the service name using:** (If asked for a password just press enter)
      
    sqlplus sys@//localhost:1521/xepdb1 as sysdba
    
**Unlock the account:** 
     
    ALTER USER JOHN ACCOUNT UNLOCK;
    
Change password when necessary:
     
    ALTER USER JOHN IDENTIFIED BY "myPassword123";
    

If you encounter problems make sure these services are running:
![[Pasted image 20240905212912.png]]
