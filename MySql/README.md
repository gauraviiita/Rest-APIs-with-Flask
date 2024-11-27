# Commands for mysql

**1. Install mysql-service**
```
  sudo apt get udpate
  sudo apt get upgrade
  sudo apt install mysql-server
```
**2. Start the mysql server**
```
  sudo systemctl start mysql.service
  sudo systemctl status mysql.service
```
**3. Check the status of server**
```
  sudo systemctl status mysql.service
```
**4. Start using mysql in ubuntu**

```
  sudo mysql
```

**5. Set the credentials**

```
  sudo mysql_secure_installation

If the above command does not help you to set the password follow this command.

  sudo mysql

  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

**6. Open mysql using password**

```
  sudo mysql -u root -p
```


## 7. Install MySQL-workbench-community

Search mysql-workbench-community on Google

https://snapcraft.io/mysql-workbench-community

Run the following command.

```
  sudo snap install mysql-workbench-community
```

Search locally MySQL workbench

**All done! Let's work now**

# Create a database

```
  sudo mysql -u root -p

  CREATE DATABASE database_name;
  SHOW DATABASES;
```

## Login to MySQL CLI:
```
  sudo mysql -u root -p
```

**Lists all databases.**
```
  SHOW DATABASES;
```

**Selects a specific database.**
```
  USE your_database;
```

**Lists all tables in the selected database.**
```
  SHOW TABLES;
```

**Shows the structure of a specific table.**
```
  DESCRIBE table_name;
```

**Fetches all data from a table.**
```
  SELECT * FROM table_name;
```
