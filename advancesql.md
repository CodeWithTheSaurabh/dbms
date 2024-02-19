0. <select * from actor;>
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
| chadwick  | boseman   | Male   |      500 |
+-----------+-----------+--------+----------+
7 rows in set (0.03 sec)



1. <delete from actor where Firstname ="Johnny";> : This command comes in help if you want to delete some rows from the table ;

mysql> delete from actor where Firstname ="Johnny";
Query OK, 1 row affected (0.06 sec)

mysql> select * from actor;
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
| chadwick  | boseman   | Male   |      500 |
+-----------+-----------+--------+----------+
6 rows in set (0.00 sec)




2. <update actor set Networth = 1000 where Firstname ="chris" and Lastname ="hemsworth";> 
  or 
2. <update actor set Networth = 1000 where Firstname ="chris" and Lastname ="hemsworth";> 
This is the best way to update table from the database.

example -> update actor set Networth = 1000 where Firstname ="chris" and Lastname ="hemsworth";
output -> +-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |     1000 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |     1000 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
| chadwick  | boseman   | Male   |      500 |
+-----------+-----------+--------+----------+
6 rows in set (0.00 sec)

# Note : Distribution of the data is the best way to handled the database . Why? becuase if you create same data in the ten tables at the same time then if you wanted to change your data in the first table then it will be the complusary for other nine tables also if you assigned the same data . So declared a primary key in every distributed data and use the same data as a foriegn key in other database table. This technique will provide you to best approch for handled the database .

3. <SELECT first_name,last_name,address FROM actor JOIN address ON actor.address_id = address.address_id > : Here first_name and last_name is assigned to the first table which name is actor and address_id is another one table which is assigned in address table. here in both table address_id is common . In address table ,address_id works as a primary key. this table has also contains real value of address. And In the second table where Actor contains columns as first_name, last_name and address_id . Here in this table address_id is works as foreign key which holding the another pair of values of table. 
                Now what is happening with this query let's discusses ?
Here we are selecting which column we wants to print by keyword SELECT and after then we used JOIN it works to add two different tables . ON keyword used to start operation what you wanted to being matched from the column.


4. <SELECT first_name,last_name,address,city FROM actor JOIN address ON actor.address_id = address.address_id JOIN city on address.city_id = city.city_id limit 10 >
: By using this method you can also join city in your output which is available in another one table this is the example of inner join venn diagram.

# note - example of right OUTER JOIN venn diagram:
5. <SELECT first_name,last_name,address FROM actor RIGHT OUTER JOIN address ON actor.address_id = address.address_id  limit 10> : this is the way to fetch the data from the right table or common part that is existing in both table . but we don't need that data which was not a part of right table and also the common part.

# note - example of left OUTER JOIN venn diagram
6.  <SELECT first_name,last_name,address FROM actor LEFT OUTER JOIN address ON actor.address_id = address.address_id  limit 10> :   this is the way to fetch the data from the LEFT table or common part that is existing in both table . but we don't need that data which was not a part of LEFT table and also the common part.