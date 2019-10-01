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

#### 1. Atomicity:<br/>

A transaction is a single unit of operation. You either execute it entirely or do not execute it at all. There cannot be partial execution. Otherwise, the transaction is aborted at the point of failure and all the previous operations are rolled back to their former state.<br/>

#### 2. Consistency:<br/>

Once the transaction is executed, it should move from one consistent state to another.<br/>


#### 3. Isolation:<br/>

Isolation: Transaction should be executed in isolation from other transactions (no Locks). During concurrent transaction execution, intermediate transaction results from simultaneously executed transactions should not be made available to each other. (Level 0,1,2,3).<br/>



#### 4. Durability:<br/>

After the successful completion of a transaction, the changes in the database should persist. Even in the case of system failures.<br/>



#### The following commands are used to control transactions.<br/>

#### 1. COMMIT<br/>

To save the changes. The COMMIT command is the transactional command used to save changes invoked by a transaction to the database. When we use any DML command like INSERT, UPDATE or DELETE, the changes made by these commands are not permanent, until the current session is closed, the changes made by these commands can be rolled back.To avoid that, we use the COMMIT command to mark the changes as permanent<br/>

Following is commit command's syntax:  <br/>

#### COMMIT;<br/>
 
#### 2. ROLLBACK<br/>

The ROLLBACK command is the transactional command used to undo transactions that have not already been saved to the database. This command can only be used to undo transactions since the last COMMIT or ROLLBACK command was issued.<br/>

Following is ROLLBACK command's syntax:  <br/>

#### ROLLBACK;<br/>

#### 3. SAVEPOINT<br/>

Creates points within the groups of transactions in which to ROLLBACK. A SAVEPOINT is a point in a transaction when you can roll the transaction back to a certain point without rolling back the entire transaction.<br/>

Following is SAVEPOINT command's syntax:  <br/>


#### SAVEPOINT SAVEPOINT_NAME;<br/><br/><br/>

Feel free to share feedback.




















