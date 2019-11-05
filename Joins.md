## [Joins in Database.](https://prayuja-teli.github.io/Blog/Joins)<br/>    

### What is join?<br/>

A Join clause is used to combine rows from two or more tables.<br/>
Join create relation based on the related or matching column between the tables.<br/>

### Why Join Is used?<br/>

Have you ever thought how to extract value from two or three different tables collectively? 
It is done using joins.<br/>


### Types of Join?<br/>

#### 1. Cross Join/Cartesian

Here two tables are crossed with each other.<br/>

Eg:<br/>

Table Student -		

| ID | Name |
| :------------- | :------------- | :------------- | 
| 1 | Alia |
| 2 | Shriya |


 Table Student_Info <br/>
   
| Student_Info- ID | Address |
| :------------- | :------------- | :------------- | 
|1 | Delhi  |
|3 | Mumbai  |


Query - <br/>

Select * from Student cross join Student_Info;<br/>

Output:<br/>

|ID  | Name  |  ID    | Address  |
| :------------- | :------------- | :------------- | 
| 1  | Alia     |    1   | Delhi |   
| 2  | Shriya   |   3   | Mumbai |
| 1  |  Alia    |      1   | Delhi |
| 2  | Shriya   |  3  | Mumbai |

###  Issue:

When multiple or huge amount of data is provided Cartesian product is not flexible solution.<br/>

### Basic Syntax:<br/>

#### Syntax for joining any two tables :<br/>

Select column_Name from table_name1 join table_name2 on table_name1.column_Name = table_name2.column_Name ;<br/>

#### Syntax for joining any three tables :<br/>

Select column_Name from table_name1 join table_name2 on table_name1.column_Name = table_name2.column_Name  join table_name3 on table_name2.column_name = table_name3.column_Name;<br/>

Here we can use aliases to represent column name rather than using complete column name.<br/>

Eg: <br/>
Select a.column_Name, b.column_Name from table_name1 a join table_name2 b on a.column_Name = b.column_Name ;<br/>


* (INNER) JOIN: (Default join)Returns records that have matching values in both tables. <br/>

OR<br/>

* Equi join - We special use “=“ in where condition;<br/>

Table Class 

|id | Name |
| :------------- | :------------- | :------------- | 
| 1 |  Shanaya | 
| 2 |  Ramesh | 

Table Class_Info

| id | Age |
| :------------- | :------------- | :------------- | 
|1 | 10 |
| 3 | 9 |

SELECT * from class INNER JOIN class_info where class.id = class_info.id;<br/>

Output:<br/>
<br/>
| Id | Name |  Age |
| :------------- | :------------- | :------------- | 
| 1 | Shanaya | 10 |

 
 
 
 
 
 
 <br/><br/><br/><br/>
 
 
 Feel free to share feedback.
