After installation open the terminal:
    
    sqlplus sys@xe as sysdba
    
During the installation of Oracle 21c XE, you are asked to set a password for the **`SYS`** and **`SYSTEM`** accounts. Typically, both accounts are set with the same password during installation, but you can specify different passwords for them if you choose.

- **`SYS`**: This account has the highest privileges and is mainly used for database administration and maintenance tasks. It has `SYSDBA` privileges.
- **`SYSTEM`**: This account has administrative privileges but is primarily used for general administrative tasks, such as managing user accounts and system settings.
===========================================================
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
    
**Create an account:** 
     
    CREATE USER JOHN ACCOUNT UNLOCK;
    
**Unlock the account:** 
     
    ALTER USER JOHN ACCOUNT UNLOCK;
    
Change password when necessary:
     
    ALTER USER JOHN IDENTIFIED BY "myPassword123";
    

If you encounter problems make sure these services are running:
![[Pasted image 20240905212912.png]]
=============================

sqlplus sys@//localhost:1521/xepdb1 as sysdba
sqlplus sys@xepdb1 as sysdba

SELECT USERNAME FROM ALL_USERS;
SELECT USERNAME FROM DBA_USERS;
SHOW CON_NAME;