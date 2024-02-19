<!-- My MYSQL PASSKEY = "sourabh@123" -->
# Basics of SQL
# How to start mysql console ?
: you have to write this command in your cmd folder < mysql -u root -p > after than you console ask you write password which you set at the time of server setting. When you entered the password your console has been started then you can put your command lines of code simultaneously.

2. <show databases; > : this command will show you how many databases files are exists in your system.
output -> mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sourabh_database   |
| sys                |
+--------------------+
5 rows in set (0.03 sec)


3.  <create database putYourDatabaseName; > By using this command you can create databases in your table.

4.  <use putYourDataBaseName; > By using this database querry you can work on perticular databases

5. <drop database putYourDatabase; > By using this command you can delete particular database in your database

6. <create table tableName (columnName1 datatype(size in number) , columnName2 datatype ); > 
By using this command you can create table in your database 
example -> create table Movies (Name varchar(100) , Rating integer);

7. <show tables ;> : you can see your table created by the database

8. insert into tableName (columnName1,columnName2) values ("Harry-Potter" , 5)
example-> insert into movies (Name,Rating) value ("ballu-bhai",5);
example-> insert into movies (Name,Rating) values ("lallu-bhai" , 4.5);
Output->mysql> select * from movies;
+--------------+--------+
| Name         | Rating |
+--------------+--------+
| Harry-potter |      5 |
| babu-bhaiya  |      5 |
| ballu-bhai   |      5 |
| lallu-bhai   |      5 |
+--------------+--------+
4 rows in set (0.00 sec)


9. <select * from tableName; > : This Command will return or print whole table which you enter the name . If you wanted to fetch data mannually from the tables you can easily access my replacing * into the column name Nd in final result you will get your expected output. 
example -> select * from movies;
Output  -> mysql> select * from Actor;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
+-----------+-----------+--------+----------+
6 rows in set (0.00 sec)


10. <insert into tableName (columnName1,columnName2) values ("Harry-Potter" , 5) ,(put another values ;) , (put again another value) . () , () ;  > : By using this command you can add multi values in the same table at the same time.
example -> insert into movies (Name,Rating) value ("ballu-bhai",5) ,("lallu-bhai" , 4.5);
output -> mysql> select * from Actor;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
+-----------+-----------+--------+----------+
6 rows in set (0.00 sec)


11. <\! cls > : This command used to clear the windows .


12. <SELECT * FROM TABLENAME WHERE TABLECOULMN = 500; > : This will helps you to select conditionalmatic columns or table.
example : SELECT * FROM ACTORS WHERE NETWORTH >=500 OR networth < 200; >
            OUTPUT => 
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Chris     | Evans    | Male   |      700 |
| Paul      | Rudd     | Male   |      150 |
| Brie      | Larson   | Female |      650 |
+-----------+----------+--------+----------+

13. <select * from actor where Gender ="Female"; > : This the another way to fetch data

mysql> select * from actor where Gender ="Female";
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Brie      | Larson   | Female |      650 |
+-----------+----------+--------+----------+
2 rows in set (0.05 sec)

14. <select Firstname,Networth from actor where Gender ="female"; > : Another way to fetch data

mysql> select Firstname,Networth from actor where Gender ="female";
+-----------+----------+
| Firstname | Networth |
+-----------+----------+
| Scarlett  |      500 |
| Brie      |      650 |
+-----------+----------+
2 rows in set (0.00 sec)


15. <select * from actor where Firstname like "ch%"; > : this is the way to fetch name with prefix

mysql> select * from actor where Firstname like "ch%";
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
| chadwick  | boseman   | Male   |      400 |
+-----------+-----------+--------+----------+
3 rows in set (0.01 sec)


16. <select * from actor where Firstname like "%is"; > : This is the way to fetch data from suffix by using keyword "like"
mysql> select * from actor where Firstname like "%is";
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
2 rows in set (0.00 sec)


17.  <select * from actor where Firstname like "%a%"; > : This is the way to fetch data of firstname if it is contained atleast "a" character in the words. -> "%a%"
mysql> select * from actor where Firstname like "%a%";
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Paul      | Rudd     | Male   |      150 |
| chadwick  | boseman  | Male   |      400 |
+-----------+----------+--------+----------+
3 rows in set (0.00 sec)


18. # order by -> < select * from actor order by networth asc >
this is the way to arrange your order in ascending order or in the descending order .

mysql> select * from actor order by networth asc;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Paul      | Rudd      | Male   |      150 |
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| chadwick  | boseman   | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Brie      | Larson    | Female |      650 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
7 rows in set (0.01 sec)


19. <select * from actor order by networth desc > : This is the way to arange your data in the descending order ;
mysql> select * from actor order by networth asc;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Paul      | Rudd      | Male   |      150 |
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| chadwick  | boseman   | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Brie      | Larson    | Female |      650 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
7 rows in set (0.00 sec)

20. <select * from actor where firstname like "%is" order by networth asc; > : By this way you can 
mysql> select * from actor where firstname like "%is" order by networth asc;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
2 rows in set (0.00 sec)

#note : if you don't mentioned any desc or asc in the command then it will automatically arrange your order in the ascending order.


21. <select * from actor where firstname like "ch%" order by firstname; > : This will order your list as in alphabetic order as you mentioned in "like"

mysql> select * from actor where firstname like "ch%" order by firstname;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| chadwick  | boseman   | Male   |      400 |
| Chris     | Hemsworth | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
3 rows in set (0.00 sec)


22. <select * from actor where firstname like "ch%" order by firstname , networth desc; >
you can also fetch your data according to the distinct order.
 mysql> select * from actor where firstname like "ch%" order by firstname , networth desc;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| chadwick  | boseman   | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
| Chris     | Hemsworth | Male   |      400 |
+-----------+-----------+--------+----------+
3 rows in set (0.00 sec)


23. # limit -: how to set pagination in the code

23. <select * from actor limit 5; > : This command creates limit in output ordering like how amazon and other website contents millions of database but still they only provide you bunches of database either ten of set or twenty of set.

mysql> select * from actor limit 5;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
+-----------+-----------+--------+----------+
5 rows in set (0.00 sec)

24. # offset -:
24. <select * from actor limit 5 offset 0; > : where offset means where you wanted to start your indexing here in the next example we put offset 0 means we have to start from the first end limit to the till 5.

let me show the completed database for better understanding ->
mysql> select * from actor;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
| chadwick  | boseman   | Male   |      400 |
+-----------+-----------+--------+----------+
7 rows in set (0.00 sec)


mysql> select * from actor limit 5 offset 0;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
+-----------+-----------+--------+----------+
5 rows in set (0.00 sec)


example :- > 2
mysql>  select * from actor limit 5 offset 2;
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Chris     | Evans    | Male   |      700 |
| Paul      | Rudd     | Male   |      150 |
| Brie      | Larson   | Female |      650 |
| chadwick  | boseman  | Male   |      400 |
+-----------+----------+--------+----------+
5 rows in set (0.00 sec)

25. <update actor set networth = 500 where Firstname = "chadwick"; > : There is the way to update your data inside the table ;

example -> update actor set networth = 500 where Firstname = "chadwick";
output ->  update actor set networth = 500 where Firstname = "chadwick";
Query OK, 1 row affected (0.03 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql>  select * from actor;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Deep      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
| chadwick  | boseman   | Male   |      500 |
+-----------+-----------+--------+----------+
7 rows in set (0.00 sec)

