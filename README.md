# Database_and_SQL-for_Data_Science_and_Python
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
       
<p>In the statement, TableName identifies the table. The ColumnName identifies the column value to be changed, as specified in the <WHERE [Condition] >. Let's look at an example. In this example, you want to update the FIRSTNAME and LASTNAME of the author with AUTHOR_ID A2 from Rav Ahuja to Lakshmi Katta. In this example, to see the UPDATE statement in action, we start by selecting all rows from the author table to see the values. To change the first name and last name to Lakshmi Katta where the AUTHOR_ID = A2, enter the UPDATE statement as follows. UPDATE AUTHOR SET LAST NAME = KATTA, FIRST NAME = LAKSHMI WHERE AUTHOR_ID = A2. Now, to see the result of the update, select all rows again from the Author table and you will see that in row to the name changed from Rav Ahuja to Lakshmi Katta. Note that if you do not specify the WHERE clause, all the rows in the table will be updated.</p>

# DELETE







