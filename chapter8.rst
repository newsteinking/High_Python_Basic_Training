chapter 8: Dictionaries
=========================================

8.1 Dictionaries
----------------------------


.. code-block:: python


    #Create and print a dictionary:
    my_car_dict = {
      "brand": "Ford",
      "model": "Mustang",
      "year": 1964
    }
    print(my_car_dict)

    #Accessing Items
    #You can access the items of a dictionary by referring to its key name, inside square brackets:
    car_model = my_car_dict["model"]
    print(car_model)


    #There is also a method called get() that will give you the same result:
    player_dict = {
      "cap_id": 101,
      "name": "Virat",
      "highest_score": 183
    }
    highest_score = player_dict.get("highest_score")
    print(highest_score)

    #You can change the value of a specific item by referring to its key name:
    player_dict["cap_id"] = 175
    print(player_dict)

    #The dict() Constructor
    dict_with_constructor = dict(brand="Ford", model="Mustang", year=1964)
    # note that keywords are not string literals
    # note the use of equals rather than colon for the assignment
    print(dict_with_constructor)

Python Programming Examples on Dictionary
--------------------------------------------


.. code-block:: python


    Python Program to Add a Key-Value Pair to the Dictionary
    Python Program to Concatenate Two Dictionaries Into One
    Python Program to Check if a Given Key Exists in a Dictionary or Not
    Python Program to Generate a Dictionary that Contains Numbers (between 1 and n) in the Form (x,x*x).
    Python Program to Sum All the Items in a Dictionary
    Python Program to Multiply All the Items in a Dictionary
    Python Program to Remove the Given Key from a Dictionary
    Python Program to Form a Dictionary from an Object of a Class
    Python Program to Map Two Lists into a Dictionary
    Python Program to Count the Frequency of Words Appearing in a String Using a Dictionary
    Python Program to Create a Dictionary with Key as First Character and Value as Words Starting with that Character
    6. Python Programming Examples on Sets
    Python Program to Count the Number of Vowels Present in a String using Sets
    Python Program to Check Common Letters in Two Input Strings
    Python Program that Displays which Letters are in the First String but not in the Second
    Python Program that Displays which Letters are Present in Both the Strings
    Python Program that Displays which Letters are in the Two Strings but not in Both



