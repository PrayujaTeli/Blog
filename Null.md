## [What is NULL?](https://prayuja-teli.github.io/Blog/Null)     

### Definition:<br/>

In databases, a common problem is, how to represent missing values. In SQL Server, this is solved with NULL. It is used to signify missing or unknown values. NULL really isn’t a specific value, a non-existent value, not a zero value or not an empty string value. Two NULL values are not equal. Null (or NULL) is a special marker used in Structured Query Language to indicate that a data value does not exist in the database. <br/>


### Storage :<br/>

There are two ways to store NULL.<br/>

Let's assume this table: create table mytable (a int, b int, c int, primary key (c));<br/>

You can explicitly insert a NULL by using INSERT INTO mytable (a, b, c) values (1, NULL, 2);<br/>
You can also omit the column in an INSERT using something like insert into mytable (a, c) values (1, 3);<br/>

### Handling NULL:<br/>

#### 1.COUNT(*)<br/>
Most aggregate functions eliminate null values in calculations; one exception is the COUNT function. When using the COUNT function against a column containing null values, the null values will be eliminated from the calculation. However, if the COUNT function uses an asterisk, it will calculate all rows regardless of null values being present.<br/>

Eg:<br/>
Table<br/>

| Column       | 
| :------------- | 
| 1 |
| NULL | 


select count() from Table;<br/>
=> 1<br/>
select count(*) from Table;<br/>
=> 2<br/>

#### 2. ISNULL<br/>

The COALESCE and ISNULL T-SQL functions are used to return the first non-null expression among the input arguments. Both are used to handle the NULL value in T-SQL. ISNULL takes two arguments and COALESCE takes more than two arguments as required.<br/>

Syntax: <br/>
ISNULL(argument1,argument2)<br/>
argument1: Expression<br/>
argument2: Replacement value<br/>
Eg:<br/>
declare @x int=null;<br/>
 Select ISNULL(@x,'0') AS ISNULL_OUTPUT<br/>
 ***************************************************<br/>
 Output : <br/>
   ISNULL_OUTPUT<br/>
       0<br/>
 --@x is null that is replaced with 0<br/>
 ***************************************************<br/>

#### 3. COALESCE<br/>
COALESCE ( arguments [1.......n ] )<br/>
n: Arguments<br/>

 declare @x int=null;<br/>
 declare @y int=null;<br/>
 declare @z int=20;<br/>
 COALESCE(@x,@y,@z,'0') as COALESE_OUTPUT<br/>
 ***************************************************<br/>
 Output : <br/>
   COALESE_OUTPUT<br/>
       20<br/>
 --First and second argument(@x and @y) are null so that COALESE return first<br/>
 --non-NULL argument as 20(a value of @z)<br/>
 ***************************************************<br/>

#### 4. NULLIF<br/>
NULLIF takes two arguments and returns NULL if the arguments are NULL otherwise return the first argument.<br/>
declare @x int=0;<br/>
select NULLIF(@x,0) as Result -- return NULL if @x is 0<br/>
**************************************<br/>
Output<br/>
Result<br/>
NULL<br/>
**************************************<br/><br/><br/>

Feel free to share the feedback.
