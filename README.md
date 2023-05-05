Download Link: https://assignmentchef.com/product/solved-csye7245-lab4-sqlalchemy
<br>
This lab demonstrates how to leverage SQL concepts through a traditional Object-Oriented Programming approach with the help of SQLAlchemy.

<strong>What is SQLAlchemy?</strong>

SQLAlchemy is the Python-SQL toolkit and Object Relational Mapper that gives application developers the flexibility of SQL. It provides a full suite of well known enterprise-level persistence patterns, designed for efficient and high-performing database access, adapted into a simple and Pythonic domain language.

The general structure can be illustrated as follows:

SQLAlchemy uses object-relational mapper (ORM), an Object-relational mapping is a method of coding that translates data between different system types using an object-oriented programming language and converting function calls to SQL statements.




<h1><strong>Dataset</strong></h1>

The lab was implemented using a sample data for loading basic customer information:




<table width="149">

 <tbody>

  <tr>

   <td width="149"><strong>Table: Customer</strong></td>

  </tr>

  <tr>

   <td width="149">+ id: number</td>

  </tr>

  <tr>

   <td width="149">+ name: string</td>

  </tr>

  <tr>

   <td width="149">+ age: number</td>

  </tr>

  <tr>

   <td width="149">+ address: string</td>

  </tr>

  <tr>

   <td width="149">+ email: string</td>

  </tr>

 </tbody>

</table>




<h1><strong>Experiment Setup</strong></h1>

The following are the prerequisite setup we made for the implementation of lab:




<ol>

 <li><strong> Installing Python on our machine using the following commands: </strong></li>

</ol>

<strong>For Ubuntu/Linux:</strong>

sudo apt install python3

sudo apt install python3-pip

<strong>For Windows:</strong>

Link for downloading Python binaries: <a href="https://www.python.org/downloads/">https://www.python.org/downloads/</a>










<ol start="2">

 <li><strong> After Python is configured, we installed SQLAlchemy:</strong></li>

</ol>

Create a new project in Pycharm and run the following commands for installation the libraries of SQLAlchemy in Python environment:




pip install sqlalchemy




pip install psycopg2-binary







<ol start="3">

 <li><strong> Setting up the relational PostgreSQL database:</strong></li>

</ol>

We downloaded the <a href="https://www.enterprisedb.com/downloads/postgres-postgresql-downloads">PostgreSQL binaries</a> and ran the executable file







<h1><strong>Tests Cases</strong></h1>

<ol>

 <li>We entered the connection parameters to connect to the PostgreSQL server instance in program base.py</li>

</ol>




<strong>Syntax:</strong> postgresql://username:<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="7202130101051d0016321a1d0106">[email protected]</a>:port/database
















After entering the connection details to the database the engine does not connect to the database instantly. This process is postponed to when it’s needed (like when we submit a query, or when create/update a row in a table). The create_engine() returns an instance of Engine, and it represents the core interface to the database, adapted through a dialect that handles the details of the database and DBAPI in use.

<ol start="2">

 <li>The customer.py is a sample Python class containing 5 attributes that we’d like to be converted to a table and attributes as its columns</li>

 <li>The main.py program inserts data using the newly created class</li>

 <li>The queries.py contains a get_all_data() function which is used to query the table and retrieve the inserted records in the output console</li>

</ol>

Apart from the get_all_data() function, the update_record() function is used to update any record based on the id using filter()




<h1><strong>Results</strong></h1>

Once the engine is created and data is inserted using main.py program, we login to pgadmin console to check if the data in inserted correctly into the intended database in our case, the data is inserted in:

<ul>

 <li>Database: postgres</li>

 <li>Table: Customer</li>

 <li>Columns: id, name, age, address, email</li>

</ul>

Further, after executing the update_record() function for changing the name with id 4, we see the changes reflected into the database with updated name from <strong>‘Jane Doe’ </strong>to <strong>‘Ryan Gosling’</strong>

<h1></h1>

<h1>Lessons Learned</h1>

<ol>

 <li>Learned how to write an object-oriented Python program which encapsulates SQL concepts, connects to a relational database and translates function calls to SQL queries.</li>

 <li>Learned how to insert data into the relational database using a Python function with the help of SQLAlchemy libraries</li>

 <li>Learned to update data from a function and retrieve the data in the Python output console without querying the database which cut downs switching back and forth between writing Python and SQL</li>

</ol>







<h1>References</h1>

<a href="https://auth0.com/blog/sqlalchemy-orm-tutorial-for-python-developers/?utm_source=medium&amp;utm_medium=sc&amp;utm_campaign=sqlalchemy_python">auth0 blog</a>

<a href="https://www.sqlalchemy.org/">https://www.sqlalchemy.org/</a>

<a href="https://docs.sqlalchemy.org/en/13/orm/tutorial.html">https://docs.sqlalchemy.org/en/13/orm/tutorial.html</a>











