# Database and SQL for Data Science and Python.
Database and SQL for Data Science with Python.- Coursera Course.

<p><b>SQL-(Structured Query Language)</b> is a language used for relational databases.</p>
<p><b>Data</b>-Facts in words, numbers and pictures. It is the biggest asset in any business.<b>Database</b> -It is a respository of data is a program that stores data. It is in use everyday.It has functionalities of adding, modifying, Querying and storing data.</p>

# Types of databases
<p><b>Relational Databases</b></p>
<p><ul><li>Data is stored in Tabular form columns and rows.</li>
       <li>Column Contain item properties e.g Lastname, FirstName.</li>
       <li>Tables is a collection of related things i.e Authors, Teachers etc.</li>
</ul></p>

<p><b>Database Management System (DBMS)</b>- A set of software tools to manage databases.</p>
<p><b>Relational Database System-(RDBMS)</b>- A set of tools that controls data access, organization and storage. Examples of RDBMS- MySQL, Oracle database, IBM db2 etc.</p>

# Basic SQL Commands
<p><ul><li>Create a Table.</li>
        <li>Insert data to a table.</li>
        <li>Select data in a table.</li>
        <li>Update data in a table.</li>
        <li>Delete data from a table.</li>
</ul></p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/8e78e55d-6f15-4cc7-a4ed-729051ed64c4)


# SELECT statement
<p>Retrieving data from the table. To see the data within the table and retrieve the rows we use the SELECT statement.<b>SELECT STATEMENT</b>-It is a data manipulation-DML statement used to read and modify data.</p>
<p>Always understand that SELECT the order of the result set depends on the order of columns in the query.</p>

# SELECT statement with WHERE
<p>The WHERE clause is used to restricting Results. Always requires a predicate which Evaluates to True, False or Unknown. Used in the search condition of Where clause. </p>
<p><b>SELECT with WHERE clause Comparison Operators</b></p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/76015fb5-9144-498a-8271-8ef3ea4b92d5)


# Useful expressions used the query SELECT- COUNT, DISTINCT,LIMIT

<p><b>COUNT</b>- This is an inbuilt database that retrieves the number of rows that match the query criteria. For example, get the total number of rows in a given table,</p>
<p>select COUNT(*) from tablename.</p> 
<p></p>Let's say you create a table called MEDALS which has a column called COUNTRY, and you want to retrieve the number of rows where the medal recipient is from Canada. You can issue a query like this:</p>
<p><b><i>Select COUNT(COUNTRY) from MEDALS where COUNTRY='CANADA.'  </i></b></p>

<p><b>DISTINCT</b>-It is used to remove duplicate values in a dataset. For example retrieve unique values from a column.</p>
<p>Example, retrieve the list of unique countries that received gold medals. That is, removing all duplicate values of the same country.</p>
<p><b><i>Select DISTINCT COUNTRY from MEDALS where MEDALTYPE = 'GOLD'.</i></b></p>

<p><b>LIMIT</b>-Restricting the number of rows in a table. <b>Select * from tablename LIMIT 10.</b> This can be very useful to examine the results set by looking at just a few rows instead of retrieving the entire result set which may be very large. Example, retrieve just a few rows in the MEDALS table for a particular year.</p>
<p><b><i>Select * from MEDALS where YEAR = 2018 LIMIT 5.</i></b></p>

# Examples of the special expressions with SELECT statement.

# COUNT
<p><b><i>1. Suppose we want to count the number of records or rows of the “FilmLocations” table.</i></b></p> 
<p><b><i>SELECT COUNT(*) FROM FilmLocations;</i>.</b></p>

<p><b><i>2. now we want to count the number of locations of the films. But we also want to restrict the output resultset in such a way that we only retrieve the number of locations of the films written by a certain writer.</i></b></p> 
<p><b><i>SELECT COUNT(Locations) FROM FilmLocations WHERE Writer="James Cameron";</i>.</b></p>

# DISTINCT
<p><b><i>1. we want to retrieve the title of all films in the table in such a way that duplicates will be discarded in the output resultset.</i></b></p>
<p><b><i>SELECT DISTINCT Title FROM FilmLocations;</i>.</b></p>

<p><b><i>2. we want to retrieve the count of release years of the films produced by a specific company in such a way that duplicate release years of those films will be discarded in the count.</i></b></p>
<p><b><i>SELECT COUNT(DISTINCT ReleaseYear) FROM FilmLocations WHERE ProductionCompany="Warner Bros. Pictures";</i></b></p>

# LIMIT
<p><b><i>1. let us retrieve a specific number of rows from the top of the table in such a way that rows other than those are not in the output resultset.</i></b></p>
<p><b><i>SELECT * FROM FilmLocations LIMIT 25;</b></p></i>

<p><b><i>2. Now we want to retrieve a specific number of rows from the table, but thid time, not from the top of the table. This time we want to retrieve a specific number of rows starting from a specific row in the table.</i></b></p>
<p><b><i>SELECT * FROM FilmLocations LIMIT 15 OFFSET 10;</i></b></p>

<p><b><i>3. Retrieve the next 3 film names distinctly after first 5 films released in 2015.</i></b></p>
<p><b><i>SELECT DISTINCT Title FROM FilmLocations WHERE ReleaseYear=2015 LIMIT 3 OFFSET 5;</i></b></p>

# INSERT Statement
<p><b>The INSERT statement</b> is used to add new rows to a table. The INSERT statement is one of the data manipulation language statements.The <b>syntax of the INSERT statement</b> looks like this, insert into table name, column name, values. In this statement, table name identifies the table, the column name list identifies each column in the table, and the values clause specifies the data values to be added to the columns in the table.</p>

# UPDATE, DELETE Statement
<p>After a table is created and populated with data, the data in a table can be altered with the UPDATE statement. The UPDATE statement is one of the data manipulation language or DML statements. DML statements are used to read and modify data.</p>

# UPDATE
<p>After a table is created and populated with data, the data in a table can be altered with the <b>UPDATE statement.</b> The UPDATE statement is one of the data manipulation language or DML statements. DML statements are used to read and modify data. Based on the author entity example, we created the table using the entity name Author and the entity attributes as the columns of the table. Rows were added to the Author table to populate the table. </p>
<p>Sometime later, you want to alter the data in the table. To alter or modify the data in the Author table, we use the UPDATE statement. The syntax of the UPDATE statement looks like this:-
<p><b><i>UPDATE [TableName] SET [ColumnName] = [Value] ]> <WHERE [Condition] >.</i></b></p> 
       
<p>In the statement, TableName identifies the table. The ColumnName identifies the column value to be changed, as specified in the <WHERE [Condition] >. Let's look at an example. In this example, you want to update the FIRSTNAME and LASTNAME of the author with AUTHOR_ID A2 from Rav Ahuja to Lakshmi Katta. In this example, to see the UPDATE statement in action, we start by selecting all rows from the author table to see the values. To change the first name and last name to Lakshmi Katta where the AUTHOR_ID = A2, enter the UPDATE statement as follows. 
       
<p><b><i>UPDATE AUTHOR SET LAST NAME = KATTA, FIRST NAME = LAKSHMI WHERE AUTHOR_ID = A2.</i></b></p> 
       
<p>Now, to see the result of the update, select all rows again from the Author table and you will see that in row to the name changed from Rav Ahuja to Lakshmi Katta. Note that if you do not specify the WHERE clause, all the rows in the table will be updated.</p>

# DELETE
<p>Sometime later, there might be a need to remove one or more rows from a table. The rows are removed with the <b>DELETE statement.</b> The DELETE statement is one of the data manipulation language statements used to read and modify data. The syntax of the DELETE statement looks like this:-

<p><b><i>DELETE FROM [TABLEName] <WHERE [Condition] >. </WHERE></i></p></b>
       
<p>The rows to be removed are specified in the WHERE condition. Based on the author entity example, we want to delete the rows for AUTHOR_ID A2 and A3. Let's look at an example. DELETE FROM AUTHOR WHERE AUTHOR_ID IN ('A2','A3'). Note that if you do not specify the WHERE clause, all the rows in the table will be removed.</p>

# INSERT Statement

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/8c3d21a2-ab9c-4825-9bb5-df0230af6a90)

<p>1. Insert a new instructor record with id 4 for Sandip Saha who lives in Edmonton, CA into the “Instructor” table.</p>
<p><b><i>INSERT INTO Instructor(ins_id, lastname, firstname, city, country)
VALUES(4, 'Saha', 'Sandip', 'Edmonton', 'CA');</i></b></p>

<p>2. Insert two new instructor records into the “Instructor” table. First record with id 5 for John Doe who lives in Sydney, AU. Second record with id 6 for Jane Doe who lives in Dhaka, BD.</p>
<p><b><i>INSERT INTO Instructor(ins_id, lastname, firstname, city, country)
VALUES(5, 'Doe', 'John', 'Sydney', 'AU'), (6, 'Doe', 'Jane', 'Dhaka', 'BD');</i></b></p>

# UPDATE Statement

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/e5947cbb-6ea4-40c7-8c48-ec9a0d3b10a0)

<p> 1.Update the city for Sandip to Toronto. </p>
<p><b><i>UPDATE Instructor</i></b></p>
<p><b><i>SET city='Toronto'</i></b></p> 
<p><b><i>WHERE firstname="Sandip"; </i></b></p>

<p>We want to update multiple columns of an existing row of the table.</p>
<p> 2.Update the city and country for Doe with id 5 to Dubai and AE respectively.</p>
<p><b><i>UPDATE Instructor</i></b></p>
<p><b><i>SET city='Dubai', country='AE' </i></b></p> 
<p><b><i>WHERE ins_id=5;</i></b></p>

# DELETE

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/02f1b22c-0d20-404e-83d0-83305d512f82)

<p>1. We want to remove a row from the table.</p>
<p>Remove the instructor record of Doe whose id is 6.</p>
<p><b><i>DELETE FROM instructor</i></b></p>
<p><b><i>WHERE ins_id = 6;</i></b></p>

<p><b>Summary & Highlights</b></p>
<p><ul><li>You can use Data Manipulation Language (DML) statements to read and modify data.</li> 
       <li>The search condition of the WHERE clause uses a predicate to refine the search.</li>  
       <li>COUNT, DISTINCT, and LIMIT are expressions that are used with SELECT statements.</li>  
       <li>INSERT, UPDATE, and DELETE are DML statements for populating and changing tables.</li> </ul></p>
       
# Introduction to Relational Databses and Tables.
<p>Relational Model</p>
<p><ul><li>Most used data model.</li>
       <li>Allows data indepedence</li>
       <li>Data is stored in Tables.</li></ul></p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/b978da9a-38e4-466f-8126-57226dee96e9)

# ENTITY-Relationship Model
<p><ul><li>Used as a tool to design relational databases.</li>
       <li>Entities have attributes within the databases which tell more about an entity.</li></ul></p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/bc7dee11-2adb-4671-b4dc-e3418718028e)

<p><ul><li>For example in the entity above 'Student' it has the attributes Firstname, Lastname age ETC</li></ul></p>

# Mapping Entity Diagrams to Tables.
<p><ul><li>Entities becomes tables.</li>
       <li>Attributes get translated into columns</li>
       <li>Each attribute has a data value made of characters, numbers or currency.</li></ul></p>

<p>Each table will be given a primary key which is a unique attribute in each table. Defines relationship to avoid duplications</p>
<p><b>Foreign Key</b> some tables may have primary keys linked to other tables.</p>

<p>Summary:-</p>
<p><ul><li>The key advantage of the relational model is data indepedence.</li>
       <li>Entities are indepedent objects which have attributes.</li>
       <li>Entities map to Tables in a Relational Database.</li>
       <li>Atrributes map to Columns in a table.</li>
       <li>Common data types include characters,numbers and dates/times.</li>
       <li>A primary Key uniquely identifies a specific row in a table.</li>
</ul></p>

# Types of SQL statements (DDL vs. DML)

<p>SQL statements are into types DDL and DML</p>
<p><b>DDL (Data Definition Language) statements: They define, change, or drop data, Objects or tables.</b></p>
<p>COMMON DDL</p>
<p><ul><li>CREATE- used to create tables and define columns</li>
       <li>ALTER- used to alter tables addding, deleting columns within a table.</li>
       <li>TRUNCATE-used to deleting data in a table and not table itself. </li>
       <li>DROP- used to deleting tables within a database</li>
</ul></p>

<p>DML (Data Manipulation Language) statements used to read and modify data. These are also referred to as CRUD operations (<b><h2>Create, Read, Update & Delete rows</b></h2>h2></p>
<p>COMMON DML</p>

<p><ul><li>INSERT- used to insert a row or rows into a table</li>
       <li>SELECT- used to select or read rows within a table.</li>
       <li>UPDATE-used to edit rows or row in a table. </li>
       <li>DELETE- used to remove or delete a row or rows from a table.</li>
</ul></p>

# CREATE TABLE Statement
<p>Create a table in relational database using Entity Name, Atrributes and the CREATE TABLE statement. </p>
<p><h2>Create table</h2></p>
<p>Most commonly used DDL statement.</p>
<p>Syntax: CREATE TABLE <i>table_name</i></p>
       <p><i>(</i></p>
       <p><i>column_name_1 datatype optional parameters,</i></p>
       <p><i>column_name_2 datatype,</i></p>
       <p>...</p>
       <p><i>column_name_n datatype</i></p>
       <p>)</p>

<p><b>CREATE A TABLE FOR PROVINCES</b></p>
<p><i>CREATE TABLE provinces(</i></p>
<p><i>idchar(2) PRIMARY KEY NOT NULL,</i></p>
<p><i>name varchar(24)</i></p>
<p>)</p>

<p><b>Create a table called Author</b></p>
<p><i>CREATE TABLE author (</i></p>
<p><i>author_id CHAR(2) PRIMARY KEY NOT NULL,</i></p>
<p><i>lastname VARCHAR(15) NOT NULL,</i></p>
<p><i>firstnamename VARCHAR(15) NOT NULL,</i></p>
<p><i>email VARCHAR(40) NOT NULL,</i></p>
<p><i>city VARCHAR(15),</i></p>
<p><i>country CHAR(2)</i></p>
<p><i>)</i></p>

# ALTER, DROP, and TRUNCATE Tables

<p><ul><li>Add or remove columns.</li>
       <li>Modify the data type of Columns</li>
       <li>Add or remove keys.</li>
       <li>Add or remove constraints.</li>
</ul></p>
<p><i>ALTER TABLE <table_name></i></p>
<p><i>ADD COLUMN <column_name_1> datatype</i></p>
<p>...</p>
<p><i>ADD COLUMN <column_name_n> datatype;</i></p>

<p>Example:-</p>
<p><i>ALTER TABLE author</i></p>
<p><i>ADD COLUMN telephone_number BIGINT;</i></p>

<p><h2>Modify Datatype of a Column</h2></p>
<p><i>ALTER TABLE <table_name></i></p>
<p><i>ALTER TABLE <table_name></i></p>
<p><i>ALTER COLUMN <column_name> SET DATATYPE</i></p>
<p><i><datatype>;</i></p>

<p><b>Example:-</b></p>
<p><i>ALTER TABLE author</i></p>
<p><i>ALTER COLUMN telephone_number SET DATA TYPE</i></p>
<p><i>CHAR(20);</i></p>

<p><i>ALTER TABLE author</i></p>
<p><i>DROP COLUMN telephone_number;</i></p>

<p><b>DROP TABLE</b></p>
<p><i>DROP TABLE <table_name>;</i></p>

<p><i>TRUNCATE TABLE <table_name></i></p>
<p><i>IMMEDIATE;</i></p>























