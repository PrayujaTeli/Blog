## [Joins in Database](https://prayuja-teli.github.io/Blog/Joins)<br/>    

### What is join?<br/>

A Join clause is used to combine rows from two or more tables.<br/>
Join create relation based on the related or matching column between the tables.<br/>

### Why Join Is used?<br/>

Have you ever thought how to extract value from two or three different tables collectively? 
It is done using joins.<br/>

### Basic Syntax:<br/>

#### Syntax for joining any two tables :<br/>

Select column_Name from table_name1 join table_name2 on table_name1.column_Name = table_name2.column_Name ;<br/>

#### Syntax for joining any three tables :<br/>

Select column_Name from table_name1 join table_name2 on table_name1.column_Name = table_name2.column_Name  join table_name3 on table_name2.column_name = table_name3.column_Name;<br/>

Here we can use aliases to represent column name rather than using complete column name.<br/>

Eg: <br/>
Select a.column_Name, b.column_Name from table_name1 a join table_name2 b on a.column_Name = b.column_Name ;<br/>

### Types of Join?<br/>

#### Cross Join/Cartesian

Here two tables are crossed with each other.<br/>

Eg:<br/>

Table Student -		

| ID | Name |
| :------------- | :------------- | 
| 1 | Alia |
| 2 | Shriya |


 Table Student_Info <br/>
   
| Student_Info- ID | Address |
| :------------- | :------------- |
|1 | Delhi  |
|3 | Mumbai  |


Query - <br/>

Select * from Student cross join Student_Info;<br/>

Output:<br/>

|ID  | Name  |  ID    | Address  |
| :------------- | :------------- | :------------- | :------------- |
| 1  | Alia     |    1   | Delhi |   
| 2  | Shriya   |   3   | Mumbai |
| 1  |  Alia    |      1   | Delhi |
| 2  | Shriya   |  3  | Mumbai |

###  Issue:

When multiple or huge amount of data is provided Cartesian product is not flexible solution.<br/>

### (INNER) JOIN:(Default join)<br/>
Returns records that have matching values in both tables. <br/>

OR <br/>

### Equi join - We special use “=“ in where condition;<br/>

Table Class 

|id | Name |
| :------------- | :------------- | 
| 1 |  Shanaya | 
| 2 |  Ramesh | 

Table Class_Info

| id | Age |
| :------------- | :------------- | 
| 1 | 10 |
| 3 | 9 |

SELECT * from class INNER JOIN class_info where class.id = class_info.id;<br/>

Output:<br/>

| Id | Name |  Age |
| :------------- | :------------- | :------------- | 
| 1 | Shanaya | 10 |

### Theta join:<br/>

They have tuples from different relations if and only if they satisfy the theta condition.<br/>

### Natural join:<br/>

At least one similar column needed in both tables.

### LEFT (OUTER) JOIN:<br/>

Returns all records from the left table, and the matched records from the right table
All rows from left table and matched rows only from right <br/>


### RIGHT (OUTER) JOIN:<br/>

Returns all records from the right table, and the matched records from the left table
All rows from right table and matched rows only from left <br/>

### FULL (OUTER) JOIN:<br/>

Returns all records when there is a match in either left or right table
All rows from right and left table;<br/>


### Self Join:<br/>

A self JOIN is a regular join, but the table is joined with itself.<br/>

Table Student<br/>

| S_ID | C_ID |   

| :------------- | :------------- |
| S1   |   C1  |
| S2   |   C2  |  
| S1   |   C2  |

Query :<br/>
select  * from student a , student b  from where  a S_ID = b. S_ID && a C_ID <> b C_ID;<br/>

### Joined Self<br/>

| S_ID | C_ID |
| :------------- | :------------- | 
| S1   |   C1 |
| S2   |   C2 |
| S1   |   C2 |

### Cross product:<br/>

| S_ID | C_ID | S_ID | C_ID |
| :------------- | :------------- | :------------- | :------------- |
|S1       | C1        |   	S1       | C1     |       
|S1       | C1        |       S2    |    C2  |
|S1       | C1        |     S1      |  C2    |
|S2       | C2 		     |       S1    |    C1  |
|S2       | C2 			    |      S2     |   C2   |
|S2       |  C2 		    |      S1     |   C2   |
|S1       |  C2 			   |      S1     |   C1   |
|S1       |    C2 		  |    S2       | C2     |
|S1       |    C2			  |      S1     |   C2   |

Output<br/>

| S_ID | C_ID | S_ID | C_ID |
| :------------- | :------------- | :------------- | :------------- |
|S1    |   C1    |     S1     |  C2  |
|S1    |    C2 		|	     S1    |  C1  |



 
 <br/><br/><br/><br/>
 
 Feel free to share feedback.
