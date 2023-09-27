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

# ALTER TABLE
<p>ALTER TABLE statements used to add or remove columns from a table, to modify the data type of columns, to add or remove keys, and to add or remove constraints. The syntax of the ALTER TABLE statement is:</p>

# ADD COLUMN syntax
<p><i>ALTER TABLE table_name</i></p>
<p><i>ADD COLUMN column_name data_type column_constraint;</i></p>

<p>For example, to add a telephone_number column to the author table in the library database, the statement will be written as:</p>
<p><i>ALTER TABLE author</i></p> 
<p><i>ADD COLUMN telephone_number BIGINT;</i></p> 

# TRUNCATE Table
<p>TRUNCATE TABLE statement are used to delete all of the rows in a table. The syntax of the statement is: </p>
<p><i>TRUNCATE TABLE table_name;</i></p>

<p>So, to truncate the author’s table, the statement will be written as:</p>
<p><i>TRUNCATE TABLE author;</i></p>

<pMySQL is a Relational Database Management System (RDBMS) designed to efficiently store, manipulate, and retrieve data.></p>

# CREATE TABLE LAB
<p>You need to create two tables, PETSALE and PET. To create the two tables PETSALE and PET, copy the code below and paste it to the textarea of the SQL page. Click Go.</p>

 <p><i>CREATE TABLE PETSALE ( </i></p>
    <p><i>ID INTEGER NOT NULL,</i></p>
    <p><i>PET CHAR(20),</i></p>
    <p><i>SALEPRICE DECIMAL(6,2),</i></p>
    <p><i>PROFIT DECIMAL(6,2),</i></p>
    <p><i>SALEDATE DATE</i></p>
    <p><i>);</i></p>
    
<p><i>CREATE TABLE PET (</i></p>
    <p><i>ID INTEGER NOT NULL,</i></p>
    <p><i>ANIMAL VARCHAR(20),</i></p>
    <p><i>QUANTITY INTEGER</i></p>
    <p><i>);</i></p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/f9db9c4b-1edd-47b6-8b59-2bf5a37ddefe)

<p>Now insert some records into the two newly created tables and show all the records of the two tables. Copy the code below and paste it to the textarea of the SQL page</p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/ba36d255-28d7-49ec-97fa-b4c4a549c6aa)

# How to Create Database on Cloud
<p>Advatanges include accessed by everyone, scalability and Disaster recovery. </p>
<p>Example of cloud based databases</p>
<p><ul>
       <li>IBM db2</li>
       <li>Databases for PostgreSQL</li>
       <li>Oracle Database Cloud service</li>
       <li>Microsoft Azure SQL Database</li>
       <li>Amazon Relational Database Service(RDS)</li>
</ul></p>

<p>Available As</p>
<p><ul>
       <li>VMs or Managed services</li>
       <li>Single or multitenant</li>
</ul></p>

# Hands-on Lab: Create Db2 service instance and Get started with the Db2 console

# SQL Cheat sheet.
<p><ul><li>CREATE TABLE <i>CREATE TABLE table_name (col1 datatype optional keyword, col2 datatype optional keyword,col3 datatype optional keyword,..., coln datatype optional keyword)</i> </li></ul></p>
<p><i><b>CREATE TABLE statement</b> is to create the table. Each column in the table is specified with its name, data type and an optional keyword which could be PRIMARY KEY, NOT NULL, etc.,</i></p>
<p><i>CREATE TABLE employee </i></p>
<p><i>( employee_id char(2) PRIMARY KEY, </i></p>
<p><i>first_name varchar(30) NOT NULL, mobile int);</i></p>

<p><ul><li>ALTER TABLE - ADD COLUMN</li></ul></p>
<p>ALTER TABLE table_name ADD COLUMN column_name_1 datatype....ADD COLUMN column_name_n datatype; </p>
<p><i><b>ALTER TABLE statement</b> is used to add the columns to a table.</i></p>
<p><i>ALTER TABLE employee ADD COLUMN income bigint;</i></p>

<p><ul><li>ALTER TABLE - ALTER COLUMN</li></ul></p>
<p>ALTER TABLE table_name ALTER COLUMN column_name_1 SET DATA TYPE datatype;</p>
<p><b>ALTER TABLE ALTER COLUMN</b>  statement is used to modify the data type of columns.</p>
<p><i>ALTER TABLE employee ALTER COLUMN mobile SET DATA TYPE CHAR(20);</i></p>

<p><ul><li>ALTER TABLE - DROP COLUMN</li></ul></p>
<p>ALTER TABLE table_name DROP COLUMN column_name_1 ;</p>
<p><b>ALTER TABLE DROP COLUMN</b>  statement is used to remove columns from a table.</p>
<p><i>ALTER TABLE employee DROP COLUMN mobile ;</i></p>

<p><ul><li>ALTER TABLE - RENAME COLUMN</li></ul><p></p>
<p>ALTER TABLE table_name RENAME COLUMN current_column_name TO new_column_name;</p>
<p><b>ALTER TABLE RENAME COLUMN</b>  statement is used to rename the columns in a table.</p>
<p><i>ALTER TABLE employee RENAME COLUMN first_name TO name ;</i></p>

<p><ul><li>TRUNCATE TABLE</li></ul><p></p>
<p>TRUNCATE TABLE table_name IMMEDIATE;</p>
<p><b>TRUNCATE TABLE statement</b> is used to delete all of the rows in a table. The IMMEDIATE specifies to process the statement immediately and that it cannot be undone.</p>
<p>TRUNCATE TABLE employee IMMEDIATE ;</p>

<p><ul><li>DROP TABLE</li></ul><p></p>
<p>DROP TABLE table_name ;</p>
<p><b>	Use the DROP TABLE statement</b> to delete a table from a database. If you delete a table that contains data, by default the data will be deleted alongside the table.</p>
<p><i>DROP TABLE employee ;</i></p>

<p><ul>
<li>A database is a repository of data that provides functionality for adding, modifying, and querying the data. </li>
<li>SQL is a language used to query or retrieve data from a relational database. </li>
<li>The Relational Model is the most used data model for databases because it allows for data independence. </li>
<li>The primary key of a relational table uniquely identifies each tuple or row, preventing duplication of data and providing a way of defining relationships between tables. </li>
<li>SQL statements fall into two different categories: Data Definition Language (DDL) statements and Data Manipulation Language (DML) statements.</li>
</ul></p>

# Using string, patterns and Ranges.
<p>Retriving data from a table without the where clause. WHERE clause requires a predicate</p>
<p>Predicate is an expression that evaluates to TRUE, FALSE or UNKNOWN</p>
<p>Use the LIKE predicate with string patterns for search</p>
<p><b>Example</b></p>
<p><i>WHERE <columnname> LIKE <stringpattern></i></p>
       
<p><i>WHERE firstname LIKE R% </i></p>

# SORTING Result Sets.
<p>Eliminate duplicates from a result set</p>

<p><b>Eliminating Duplicates - DISTINCT clause</b></p>
<p>Example:</p>
<p><i>select COUNTRY from Author ORDER BY 1- <b>This statement displays all the countries shown by alphabetical order.</b></i></p>

# DISTINCT CLAUSE
<p>To eliminate duplicates within a dataset we use the DISTINCT clause</p>
<p>Example:-</p>
<p><i>select DISTINCT (country) from Author</i></p>

# GROUP BY Clause
<p>It counts the particular countries</p>
<p><i>select country, count(country) from Author GROUP BY country</i></p>
<p>Using the as count Keyword to have the derivative column named. this will be as:</p>
<p><i>select country, count(country) as Count from Author group by country</i></p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/7169491d-5162-4a07-922c-db3882e98afb)

# Restricting the Result Set- HAVING clause
<p>We can check if there are more that 3 authors in a certain country</p>
<p><b>Initial Query is <i> select country, count(country) as Count from Author group by country</i></b></p>
<p><b>Second Query with having keyword <i>select country, count(country) as Count from Author group by country having count(country) > 4 </i></b></p>
<p>HAVING keyword works only with the group by statement</p>

![image](https://github.com/KennethNjuguna/Database_and_SQL-for_Data_Science_and_Python/assets/97665556/cae1d63a-4b64-451d-a5ab-56a748c6c369)

# HANDS ON LAB String Patterns, Sorting and Grouping in MySQL using phpMyAdmin

<p><b>We will use the HR Database</b></p>
<p><b> 1. Retrieve all employees whose address is in Elgin,IL</b></p>
<p><i>SELECT F_NAME , L_NAME</i></p>
<p><i>FROM EMPLOYEES</i></p>
<p><i>WHERE ADDRESS LIKE '%Elgin,IL%';</i></p>

<p><b> 2. Retrieve all employees who were born during the 1970’s.</b></p>
<p><i>SELECT F_NAME , L_NAME</i></p>
<p><i>FROM EMPLOYEES</i></p>
<p><i>WHERE B_DATE LIKE '197%';</i></p>

<p><b> 3. Retrieve all employees in department 5 whose salary is between 60000 and 70000.</b></p>
<p><i>SELECT *</i></p>
<p><i>FROM EMPLOYEES</i></p>
<p><i>WHERE (SALARY BETWEEN 60000 AND 70000) AND DEP_ID = 5;</i></p>

# SUMMARY 
<ul>
       <li>You can use the WHERE clause to refine your query results.</li>
       <li>You can use the wildcard character (%) as a substitute for unknown characters in a pattern.</li>
       <li>You can use BETWEEN ... AND ... to specify a range of numbers.</li>
       <li>You can sort query results into ascending or descending order, using the ORDER BY clause to specify the column to sort on.            </li>
       <li>You can group query results by using the GROUP BY clause. </li>
</ul>

# SQL Cheat Sheet: Intermediate - LIKE, ORDER BY, GROUP BY

# <h2>LIKE </h2>
<p>Syntax: - </p> 
 <p></p><i> SELECT column1, column2, ... FROM table_name WHERE columnN LIKE pattern; </i></p>
 <p>Description: LIKE operator is used in a WHERE clause to search for a specified pattern in a column.
There are two wildcards often used in conjunction with the LIKE operator which are percent sign(%) and underscore sign (_).  </p>
<p>EXAMPLE:</p>
<p><i>SELECT f_name , l_name FROM employees WHERE address LIKE '%Elgin,IL%';</i></p>

# <h2>BETWEEN </h2>










































