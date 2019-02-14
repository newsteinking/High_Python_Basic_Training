chapter 11: Statements
====================================



11.1 if statement
----------------------------


.. code-block:: python


    a = 33
    b = 200

    if b > a:
      print("b is greater than a")


11.2 elif
----------------------------


.. code-block:: python

    a = 33
    b = 33
    if b > a:
      print("b is greater than a")
    elif a == b:
      print("a and b are equal")

11.3 else
----------------------------


.. code-block:: python

    a = 200
    b = 33
    if b > a:
      print("b is greater than a")
      print("inside if")
    elif a == b:
      print("a and b are equal")
      print("inside el if");
    else:
      print("a is greater than b")
      print('inside else');

11.4 loops
----------------------------


.. code-block:: python

    #Python has two primitive loop commands:
    # 1.while loops
    # 2.for loops

    #While - With the while loop we can execute a set of statements as long as a condition is true.

    i = 1
    while i < 6:
      print(i)
      i += 1
    print("===================================================");
    #For - A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string)
    fruits = ["apple", "banana", "cherry"]
    for fruit in fruits:
      print(fruit)

    #The range() Function - To loop through a set of code a specified number of times, we can use the range() function,
    #The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and ends at a specified number.
    print("====================================================")
    for i in range(6):
      print(i)

    #The range() function defaults to 0 as a starting value, however it is possible to specify the starting value by adding a parameter: range(2, 6), which means values from 2 to 6 (but not including 6):
    print("====================================================")
    for i in range(2, 6):
      print(i)

    #The range() function defaults to increment the sequence by 1, however it is possible to specify the increment value by adding a third parameter: range(2, 30, 3):
    print("=====================================================")
    for i in range(2, 30, 3):
      print(i)

    #Else in For Loop
    #The else keyword in a for loop specifies a block of code to be executed when the loop is finished:
    print("=====================================================")
    for i in range(10):
      print(i)
    else:
      print("Finally finished!")

    #Nested Loops
    #A nested loop is a loop inside a loop.
    #The "inner loop" will be executed one time for each iteration of the "outer loop":
    print("======================================================");
    adj = ["red", "big", "tasty"]
    fruits = ["apple", "banana", "cherry"]

    for x in adj:
      for y in fruits:
        print(x, y)



11.5 shorthandifelse
----------------------------


.. code-block:: python


    #Short Hand If
    #If you have only one statement to execute, you can put it on the same line as the if statement.
    a = 200
    b = 33
    if a > b: print("a is greater than b")