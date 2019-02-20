chapter 2: Strings
=====================================


2.1 basic string
----------------------------


.. code-block:: python

    first_name = "Sudhir"
    last_name = "Sapkal"

    print("My Name Is "+first_name+" "+last_name)


2.2 indexing slicing
----------------------------


.. code-block:: python

    #Get the character at position 1 (remember that the first character has the position 0):

    #Substring. Get the characters from position 2 to position 5 (not included)


    my_name = "Sudhir Sapkal"

    #Indexing can be done on String
    print(my_name[1])

    #Slicing can be done on string
    print(my_name[2:5])



2.3 input from user
----------------------------


.. code-block:: python

    print("Enter Your Name")
    name = input()
    print("Hello, " + name)

2.4 print formating with string
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



2.5 properties and method of string
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


Python Programming Examples on Strings
-----------------------------------------


.. code-block:: python

    Python Program to Replace all Occurrences of ‘a’ with $ in a String
    Python Program to Remove the nth Index Character from a Non-Empty String
    Python Program to Detect if Two Strings are Anagrams
    Python Program to Form a New String where the First Character and the Last Character have been Exchanged
    Python Program to Count the Number of Vowels in a String
    Python Program to Take in a String and Replace Every Blank Space with Hyphen
    Python Program to Calculate the Length of a String Without Using a Library Function
    Python Program to Remove the Characters of Odd Index Values in a String
    Python Program to Calculate the Number of Words and the Number of Characters Present in a String
    Python Program to Take in Two Strings and Display the Larger String without Using Built-in Functions
    Python Program to Count Number of Lowercase Characters in a String
    Python Program to Check if a String is a Palindrome or Not
    Python Program to Calculate the Number of Upper Case Letters and Lower Case Letters in a String
    Python Program to Check if a String is a Pangram or Not
    Python Program to Accept a Hyphen Separated Sequence of Words as Input and Print the Words in a Hyphen-Separated Sequence after Sorting them Alphabetically
    Python Program to Calculate the Number of Digits and Letters in a String
    Python Program to Form a New String Made of the First 2 and Last 2 characters From a Given String
    Python Program to Count the Occurrences of Each Word in a Given String Sentence
    Python Program to Check if a Substring is Present in a Given String

