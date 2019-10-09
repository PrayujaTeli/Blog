## [How dates are stored and handled in database?](https://prayuja-teli.github.io/Blog/Date)     


### Storage of dates in database:<br/>

To store date and time need to convert it into a decimal value where the "date" is the integer portion of the decimal value, and the "time" is the fractional value. Internally dates are stored as 2 integers.Storing the data in two separate columns means you'll need to combine both column values any time you want to see if a given point in time is earlier or later than the stored value. If you store the values separately, you'll invariably run into "bugs" that are difficult to detect.<br/>


#### Format:<br/>

DATE - format YYYY-MM-DD<br/>
DATETIME - format: YYYY-MM-DD HH:MI:SS<br/>



DATE: A three-byte integer packed as YYYY×16×32 + MM×32 + DD<br/>

Eg: 1997-01-01 <br/>

Calculation: 1997×16×32 + 01×32 + 01 = 1022464 + 32 + 01 = 1022497

TIME: A three-byte integer packed as DD×24×3600 + HH×3600 + MM×60 + SS<br/>

Eg: 10:00:00 <br/>

Calculation: 01×24×3600 + 10×3600 + 00×60 + 00 = 86400 + 3600 + 0 + 0 = 90000



#### Database structure and query:<br/>

we have the following "Orders" table:<br/>


|OrderId     |  ProductName  |  OrderDate    | 
| :------------- | :------------- | :------------- | 
| 1 |   Geitost   |    2008-11-11   |
| 2 |   Camembert Pierrot   | 2008-11-09      |
| 3 |   Mozzarella di Giovanni  |   2008-11-11    |
| 4 |   Mascarpone Fabiola | 2008-10-29 |


Now we want to select the records with an OrderDate of "2008-11-11" from the table above.<br/>
We use the following SELECT statement:<br/><br/>
#### SELECT * FROM Orders WHERE OrderDate='2008-11-11'<br/><br/>
The result-set will look like this:<br/>

|OrderId     |  ProductName  |  OrderDate    | 
| :------------- | :------------- | :------------- |
| 1 |   Geitost   |    2008-11-11   |
| 3 |   Mozzarella di Giovanni  |   2008-11-11    |

<br/>
Feel free to share feedback.
