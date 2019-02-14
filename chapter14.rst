chapter 14: Mysql with Python
==============================================



14.1 demo mysql test
----------------------------


.. code-block:: python

    import mysql.connector


14.2 Create Connection
----------------------------


.. code-block:: python


    import mysql.connector

    mydb = mysql.connector.connect(
      host="localhost",
      user="root",
      passwd="root"
    )

    print(mydb);



14.3 Create Database
----------------------------


.. code-block:: python

    import mysql.connector

    mydb = mysql.connector.connect(
      host="localhost",
      user="root",
      passwd="root"
    )

    mycursor = mydb.cursor()

    mycursor.execute("CREATE DATABASE mypython_test_db")


14.4 Check DB Exist
----------------------------


.. code-block:: python

    import mysql.connector

    mydb = mysql.connector.connect(
      host="localhost",
      user="root",
      passwd="root"
    )

    mycursor = mydb.cursor()
    mycursor.execute("SHOW DATABASES")

    for x in mycursor:
      print(x)


14.5 ConnectToDB
----------------------------


.. code-block:: python

    import mysql.connector
    #Create Connection to DB
    mydb = mysql.connector.connect(
      host="localhost",
      user="root",
      passwd="root",
      database="mypython_test_db"
    )


    mycursor = mydb.cursor()
    mycursor.execute("CREATE TABLE employee (name VARCHAR(255), address VARCHAR(255))")


14.6 Insert
----------------------------


.. code-block:: python


    import mysql.connector

    mydb = mysql.connector.connect(
      host="localhost",
      user="root",
      passwd="root",
      database="mypython_test_db"
    )

    mycursor = mydb.cursor()

    sql = "INSERT INTO employee (name, address) VALUES (%s, %s)"
    val = ("Rohan", "Jhakle")
    mycursor.execute(sql, val)

    mydb.commit()

    print(mycursor.rowcount, "record inserted.")


14.7 Select
----------------------------


.. code-block:: python

    import mysql.connector

    mydb = mysql.connector.connect(
      host="localhost",
      user="root",
      passwd="root",
      database="mypython_test_db"
    )

    mycursor = mydb.cursor()

    mycursor.execute("SELECT * FROM employee")

    myresult = mycursor.fetchall()
    print("**************All Records*******")
    for x in myresult:
      print(x)

    #Where Condition

    sql1 = "SELECT * FROM employee WHERE address ='Pune'"

    mycursor.execute(sql1)

    myresult = mycursor.fetchall()
    print("***********Records which satisfy where condition ***********")
    for x in myresult:
      print(x)

    print("**********Record which have 'a' in name************")
    sql2 = "SELECT * FROM employee WHERE name LIKE '%ha%'"

    mycursor.execute(sql2)

    myresult = mycursor.fetchall()

    for x in myresult:
      print(x)

    #Prevent SQL Injection

    print("**********Prevent SQL Injection******************************");
    sql3 = "SELECT * FROM employee WHERE name = %s"
    name = ("Salman Khan", )

    mycursor.execute(sql3, name)

    myresult = mycursor.fetchall()

    for x in myresult:
      print(x)

    print("********Order By**************");
    sql4 = "SELECT * FROM employee ORDER BY name"
    #To have DESC order give DESC after the name in above query
    mycursor.execute(sql4)

    myresult = mycursor.fetchall()

    for x in myresult:
      print(x)

    print("**************Delete Record************************")
    sql5 = "DELETE FROM employee WHERE name = 'Amey Wagh'"
    mycursor.execute(sql5)
    mydb.commit()
    #Notice the statement: mydb.commit(). It is required to make the changes, otherwise no changes are made to the table.
    #Notice the WHERE clause in the DELETE syntax: The WHERE clause specifies which record(s) that should be deleted. If you omit the WHERE clause, all records will be deleted!
    print(mycursor.rowcount, "record(s) deleted")
