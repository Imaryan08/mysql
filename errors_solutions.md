## to run sql in gitbash
 - winpty mysql -u username -p
 - Hit "ENTER' after this command and then you'll prompt window where you have to type your password.

## To clear sql screen
 - system cls
 - system clear
 - system \! clear
 - system \! cls 

## exit from mysql terminal
 - exit

## error while connecting mysql with nodeJS 
 - error: Error: ER_NOT_SUPPORTED_AUTH_MODE: Client does
 not support authentication protocol requested
 by server; consider upgrading MySQL client

 - Solution : 
   - ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
   ```bash
   - Execute the following query in MYSQL Workbench

	ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

	Where root as your user localhost as your URL and password as your password

	Then run this query to refresh privileges:

	flush privileges;
	```

  ## another way
  1. Open MySQL Workbench and connect to your MySQL server.
  2. In the SQL Editor window, paste the following query:

  ```bash
  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

```

- After executing the query, you can run the following command to refresh the privileges:
```bash
	FLUSH PRIVILEGES;
```

![Link for this solution](https://stackoverflow.com/questions/50093144/mysql-8-0-client-does-not-support-authentication-protocol-requested-by-server?page=1&tab=scoredesc#tab-top)
