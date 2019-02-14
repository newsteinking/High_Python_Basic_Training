chapter 3: Strings
=====================================


3.1 basic string
----------------------------


.. code-block:: python

    first_name = "Sudhir"
    last_name = "Sapkal"

    print("My Name Is "+first_name+" "+last_name)


3.2 indexing slicing
----------------------------


.. code-block:: python

    #Get the character at position 1 (remember that the first character has the position 0):

    #Substring. Get the characters from position 2 to position 5 (not included)


    my_name = "Sudhir Sapkal"

    #Indexing can be done on String
    print(my_name[1])

    #Slicing can be done on string
    print(my_name[2:5])



3.3 input from user
----------------------------


.. code-block:: python

    print("Enter Your Name")
    name = input()
    print("Hello, " + name)

3.4 print formating with string
----------------------------------


.. code-block:: python

    print("This is print formating, So I am gonna Insert String here {}".format('INSERTED'));

    #This will be usefull when you wanted to do something like below
    print("Hey {} Your college {} is Super Awesome !".format('Sudhir',"TKIET"))

    #Here the replacement order can be passed in interpolation
    print("My Name is {1} {0}".format('Sudhir','Sapkal'))

    #We can also assign a variable names and replace the string accordingly

    print("My Name is {first_name} {last_name}".format(first_name='Sudhir', last_name='Sapkal'))

    #f formatted string litterls
    name = 'Sudhir'
    age = 25
    print(f'{name} is  {age} years old');



3.5 properties and method of string
----------------------------------------


.. code-block:: python

    #strip()
    a = " Hello, World! "
    print(a.strip()) # returns "Hello, World!"

    #len()
    a = "Hello, World!"
    print(len(a)) # returns length

    #lower()
    a = "Hello, World!"
    print(a.lower()) # makes all string lower case

    #upper()
    a = "Hello, World!"
    print(a.upper()) # makes all string upper case

    #replace()
    a = "Hay Hello, World"
    print(a.replace("H", "J")) # replaces H with J

    #split()
    a = "Hello, World!"
    print(a.split(",")) # returns ['Hello', ' World!']
