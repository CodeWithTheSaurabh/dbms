<!-- In this file I solved to question of hackerank and did some concept  -->
// QUESTION 01 ->
1. Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:

Equilateral: It's a triangle with  sides of equal length.
Isosceles: It's a triangle with  sides of equal length.
Scalene: It's a triangle with  sides of differing lengths.
Not A Triangle: The given values of A, B, and C don't form a triangle.
Input Format

The TRIANGLES table is described as follows:
INPUT ->
A     B      C 
20    20    23
20    20    20
20    21    22
13    14    30 

OUTPUT ->
Isosceles
Equilateral
Scalene
Not A Triangle

 Solution -> 

SELECT 
CASE
WHEN A + B > C AND B + C > A AND A + C > B
CASE
WHEN A = B AND B = C THEN 'EQUILATERAL TRIANGLE'
WHEN A = B OR B = C OR C = A THEN 'ISOSCELOUS TRIANGLE'
ELSE 'SCELANE TRIANGLE'
END
ELSE 'NOT A TRIANGLE'
END
FROM TRIANGLES;
--------------------------------------------------------------------------------------------------

// QUESTION 02 -> 
Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.
The STATION table is described as follows:

Sample Input =>

For example, CITY has four entries: DEF, ABC, PQRS and WXY.

Sample Output =>

ABC 3
PQRS 4

SOLUTION =>
SELECT CITY, LENGTH(CITY) AS LEN FROM STATION ORDER BY LEN,CITY LIMIT 1 ;
SELECT CITY, LENGTH(CITY) AS LEN FROM STATION ORDER BY LEN DESC LIMIT 1 ;

--------------------------------------------------------------------------------------------------

# GROUP BY -:
select distinct district from address;
select count(*), district from address group by district limit 10;
select count(*) as count, district from address group by district having count >= 5;
// you can applied this command in sql for exploring more

This queries will helps you to understand that how you can applied fundamental operation on single column using "group by" keyword

# having -> 
if there is operation or condition in your querry for the particular row and where u used "group by" keyword then at this place you must be done this all operation by using the keyword "having" . According to your kind of information you can not be used "where" keyword it will definetly through error. 

