# command

### login mysql
mysql -h localhost -P 3306 -u root -proot

### exit mysql
exit;

### view mysql version
select version;

### view all database
show databases;

### use database
use database_name;

### view all tables
show tables;

### view tables from another database
show tables from database_name;

### view tables struct
desc table_name;

### query mysql all character
show character set;

### query mysql all sort
show collation;

### view database support storage engine
### 1.innodb (many data delete, add, update)
### 2.mylSAM (many data read, write)
show engine;

### set character
set_character_set_database = utf8;

### set character on the server
set_character_set_server = utf8;

### view us using character 
show variables like 'character%';

### view us using sort
show variables like 'collation';