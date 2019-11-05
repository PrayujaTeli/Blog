## [Joins in Database.](https://prayuja-teli.github.io/Blog/Joins)<br/>    

### What is join?<br/>

A Join clause is used to combine rows from two or more tables.<br/>
Join create relation based on the related or matching column between the tables.<br/>

### Why Join Is used?<br/>

Have you ever thought how to extract value from two or three different tables collectively? 
It is done using joins.<br/>


### Types of Join?<br/>

Here two tables are crossed with each other .<br/>

Eg:
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


<br/>
Query - 
Select * from Student cross join Student_Info;
<br/>
Output:

|ID  | Name  | |  ID    | Address  |
| :------------- | :------------- | :------------- | 
| 1  | Alia     |    1   | Delhi |   
| 2  | Shriya   |   3   | Mumbai
| 1  |  Alia    |      1   | Delhi |
| 2  | Shriya   |  3  | Mumbai |

 
 
 <br/><br/><br/><br/>
 
 
 Feel free to share feedback.
