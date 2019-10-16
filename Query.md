## [How database parse query?](https://prayuja-teli.github.io/Blog/Query)     


### Before Parsing 

The query parsing probes are triggered before the original SQL statement is parsed.


query-parse-start: <br/>

Triggered just before the statement is parsed by the MySQL query parser. The single argument, query, is a string containing the full text of the original query.

query-parse-done:<br/>

Triggered when the parsing of the original statement has been completed. The status is an integer describing the status of the operation. A 0 indicates that the query was successfully parsed. A 1 indicates that the parsing of the query failed.


### SQL Parsing:<br/>

The parsing stage involves separating the pieces of a SQL statement into a data structure that other routines can process. The database parses a statement when instructed by the application, which means that only the application­, and not the database itself, can reduce the number of parses.<br/>

When an application issues a SQL statement, the application makes a parse call to the database to prepare the statement for execution. The parse call opens or creates a cursor, which is a handle for the session-specific private SQL area that holds a parsed SQL statement and other processing information. The cursor and private SQL area are in the program global area (PGA).<br/>



The parsing of a query is performed within the database using the Optimizer component. The Optimizer evaluates many different attributes of the given query i.e. number of tables involved, whether we have indexes available or not, what kind of expressions are involved, etc. Taking all of these inputs into consideration, the Optimizer decides the best possible way to execute the query. This information is stored within the SGA in the Library Cache – a sub-pool within the Shared Pool.

There are two possible states for a query’s processing information. One, that it can be found in the Library Cache and two, that it may not be found. The memory area within the Library Cache in which the information about a query’s processing is kept is called the Cursor. Thus if a reusable cursor is found within the library cache, it’s just a matter of picking it up and using it to execute the statement. This is called Soft Parsing. If it’s not possible to find a reusable cursor or if the query has never been executed before, query optimization is required. This is called Hard Parsing.



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

During the parse, the database performs a shared pool check to determine whether it can skip resource-intensive steps of statement processing.<br/>

To this end, the database uses a hashing algorithm to generate a hash value for every SQL statement.<br/>
When a user submits a SQL statement, the database searches the shared SQL area to see if an existing parsed statement has the same hash value. The hash value of a SQL statement is distinct from the following values:<br/>

Memory address for the statement<br/>

Hash value of an execution plan for the statement<br/>

A SQL statement can have multiple plans in the shared pool. Typically, each plan has a different hash value. If the same SQL ID has multiple plan hash values, then the database knows that multiple plans exist for this SQL ID.<br/>


Parse operations fall into the following categories, depending on the type of statement submitted and the result of the hash check:<br/>

####  Hard parse<br/>

If Oracle Database cannot reuse existing code, then it must build a new executable version of the application code. This operation is known as a hard parse, or a library cache miss.<br/>

Hard parsing means that either the cursor was not found in the library cache or it was found but was invalidated for some reason.

####  Soft parse<br/>

A soft parse is any parse that is not a hard parse. If the submitted statement is the same as a reusable SQL statement in the shared pool, then Oracle Database reuses the existing code. This reuse of code is also called a library cache hit.<br/>

Soft parses can vary in how much work they perform. For example, configuring the session shared SQL area can sometimes reduce the amount of latching in the soft parses, making them "softer."<br/><br/><br/>


Feel free to share feedback.
