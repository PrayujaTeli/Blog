## [Transaction and its properties.](https://prayuja-teli.github.io/Blog/Properties)<br/>    

### Definition:<br/>

A transaction can be defined as a group of tasks. A single task is the minimum processing unit which cannot be divided further.<br/>
 
#### SET TRANSACTION [ READ WRITE | READ ONLY ];<br/>
Let’s take an example of a simple transaction. Suppose a bank employee transfers Rs 500 from A's account to B's account. 
This very simple and small transaction involves several low-level tasks.<br/>

A’s Account<br/>
Open_Account(A)<br/>
Old_Balance = A.balance<br/>
New_Balance = Old_Balance - 500<br/>
A.balance = New_Balance<br/>
Close_Account(A)<br/>
 
B’s Account<br/>
Open_Account(B)<br/>
Old_Balance = B.balance<br/>
New_Balance = Old_Balance + 500<br/>
B.balance = New_Balance<br/>
Close_Account(B)<br/>

### Property of Transaction.<br/>

### 1. Atomicity:<;<br/>



### 2. Consistency:<br/>



### 3. Isolation:<br/>





### 4. Durability:<br/>
























Feel free to share feedback.
