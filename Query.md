## [How database parse query?](https://prayuja-teli.github.io/Blog/Query)     


### SQL Parsing:<br/>

The parsing stage involves separating the pieces of a SQL statement into a data structure that other routines can process. The database parses a statement when instructed by the application, which means that only the application­, and not the database itself, can reduce the number of parses.<br/>

When an application issues a SQL statement, the application makes a parse call to the database to prepare the statement for execution. The parse call opens or creates a cursor, which is a handle for the session-specific private SQL area that holds a parsed SQL statement and other processing information. The cursor and private SQL area are in the program global area (PGA).<br/>

During the parse call, the database performs the following checks:<br/>

#### 1. Syntax Check<br/>

A statement that breaks a rule for well-formed SQL syntax fails the check. For example, the following statement fails because the keyword FROM is misspelled as FORM:<br/>

SQL> SELECT * FORM employees;<br/>
SELECT * FORM employees<br/>
       <br/>
ERROR at line 1:<br/>
ORA-00923: FROM keyword not found where expected<br/>

#### 2. Semantic Check<br/>

The semantics of a statement are its meaning. A semantic check determines whether a statement is meaningful, for example, whether the objects and columns in the statement exist. <br/>

A syntactically correct statement can fail a semantic check, as shown in the following example of a query of a nonexistent table: <br/>

SQL> SELECT * FROM nonexistent_table; <br/>
SELECT * FROM nonexistent_table <br/>
           <br/>
ERROR at line 1: <br/>
ORA-00942: table or view does not exist <br/>

#### 3. Shared Pool Check<br/>


Feel free to share feedback.
