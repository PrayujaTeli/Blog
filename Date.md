## [How dates are stored and handled in database?](https://prayuja-teli.github.io/Blog/Date)     


### Storage of dates in database:<br/>

A common way of storing date/time is by converting it into a decimal value where the "date" is the integer portion of the decimal value, and the "time" is the fractional value. Internally dates are stored as 2 integers. The first integer is the number of dates before or after the base date (1900/01/01). The second integer stores the number of clock ticks after midnight, each tick is 1⁄300 of a second. So, September 20th, 2016 9:34:00 is stored as 42631.39861. 42631 is the number of days since .39861 is the portion of time elapsed since midnight. Storing the data in two separate columns means you'll need to combine both column values any time you want to see if a given point in time is earlier or later than the stored value. If you store the values separately, you'll invariably run into "bugs" that are difficult to detect.<br/>

#### Format:

DATE - format YYYY-MM-DD<br/>
DATETIME - format: YYYY-MM-DD HH:MI:SS<br/>

#### Eg:<br/>

we have the following "Orders" table:<br/>

|OrderId     |  ProductName  |  OrderDate    | 
| :------------- | :------------- | :------------- | 
| 1 |   Geitost   |    2008-11-11   |
| 2 |   Camembert Pierrot   | 2008-11-09      |
| 3 |   Mozzarella di Giovanni  |   2008-11-11    |
| 4 |   Mascarpone Fabiola | 2008-10-29 |


Now we want to select the records with an OrderDate of "2008-11-11" from the table above.<br/>
We use the following SELECT statement:<br/>
SELECT * FROM Orders WHERE OrderDate='2008-11-11'<br/>
The result-set will look like this:<br/>

|OrderId     |  ProductName  |  OrderDate    | 
| :------------- | :------------- | :------------- |
| 1 |   Geitost   |    2008-11-11   |
| 3 |   Mozzarella di Giovanni  |   2008-11-11    |

 
 
In order to run a MySQL Insert command and add the current date into your table, you can use MySQL's built-in function CURDATE() in your query.<br/>

An example of how to Insert a Date in MySQL using CURDATE<br/>
#### $query_auto = "INSERT INTO tablename (col_name, col_date) VALUE ('DATE: Auto CURDATE()', CURDATE() )";<br/>
Also, you can run a query to set the date manually<br/>
An example of how to Insert a Date in MySQL manually<br/>
#### $query_manual = "INSERT INTO tablename (col_name, col_date) VALUES ('DATE: Manual Date', '2008-7-04')";<br/>


### Insert a date in MySQL using YEAR<br/>
 
An example of how to Insert a YEAR in MySQL using CURDATE<br/><br/>

INSERT INTO phonebook (col_name, col_date) VALUE ('YEAR: Auto CURDATE()', CURDATE() )";<br/>
Set a date in MySQL using DATETIME<br/><br/>

Using DATETIME you can store both the date and the time. Its format is YYYY-MM-DD HH:mm:SS. Using this statement you can store the output for both DATE and TIME statements. Also, you can choose to store the date information only, but you can't store just the time.<br/><br/>

An example of how to use DATETIME<br/><br/>

INSERT INTO phonebook (col_name, col_date) VALUE ('DATETIME: Auto CURDATE()', CURDATE() )";<br/><br/><br/><br/>


Feel free to share feedback.
