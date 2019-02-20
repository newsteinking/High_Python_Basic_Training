chapter 4: List
================================================

4.1 List
----------------------------


.. code-block:: python


    my_list = ["1", 2, "hello"]
    print(my_list)

    #You access the list items by referring to the index number:
    fruit_list = ["apple", "banana", "cherry"]
    print(fruit_list[1])

    #To change the value of a specific item, refer to the index number:

    fruit_list[1] = "blackcurrant"
    print(fruit_list)

    #You can loop through the list items by using a for loop:
    for x in fruit_list:
      print(x)

    #To determine if a specified item is present in a list use the in keyword:

    if "apple" in fruit_list:
      print("Yes, 'apple' is in the fruits list")

    #To determine how many items a list have, use the len() method:

    print(len(fruit_list))

    #To add an item to the end of the list, use the append() method:

    fruit_list.append("orange")
    print(fruit_list)

    #To add an item at the specified index, use the insert() method:

    fruit_list.insert(1, "orange")
    print(fruit_list)

    #There are several methods to remove items from a list:
    fruit_list.remove("blackcurrant")
    print(fruit_list)

    fruit_list.pop()
    print(fruit_list)

    # To delet item in list
    del fruit_list[0]
    print(fruit_list)

    #The clear() method empties the list:
    fruit_list.clear()
    print(fruit_list)

    #The del keyword can also delete the list completely:
    fruit_list["23","44","66"]
    del fruit_list
    # print(fruit_list) If we try to execute this it will give error of undefine list

    #It is also possible to use the list() constructor to make a list
    fruit_list = list(("apple", "banana", "cherry")) # note the double round-brackets
    print(fruit_list)

    #Python has a set of built-in methods that you can use on lists.


Python Programming Examples on Lists
------------------------------------------

.. code-block:: python


    Python Program to Find the Largest Number in a List
    Python Program to Find the Second Largest Number in a List
    Python Program to Put Even and Odd elements in a List into Two Different Lists
    Python Program to Merge Two Lists and Sort it
    Python Program to Sort the List According to the Second Element in Sublist
    Python Program to Find the Second Largest Number in a List Using Bubble Sort
    Python Program to Sort a List According to the Length of the Elements
    Python Program to Find the Union of two Lists
    Python Program to Find the Intersection of Two Lists
    Python Program to Create a List of Tuples with the First Element as the Number and Second Element as the Square of the Number
    Python Program to Find all Numbers in a Range which are Perfect Squares and Sum of all Digits in the Number is Less than 10
    Python Program to Find the Cumulative Sum of a List where the ith Element is the Sum of the First i+1 Elements From The Original List
    Python Program to Generate Random Numbers from 1 to 20 and Append Them to the List
    Python program to Sort a List of Tuples in Increasing Order by the Last Element in Each Tuple
    Python Program to Swap the First and Last Value of a List
    Python Program to Remove the Duplicate Items from a List
    Python Program to Read a List of Words and Return the Length of the Longest One
    Python Program to Remove the ith Occurrence of the Given Word in a List where Words can Repeat
    Python Program to Remove All Tuples in a List of Tuples with the USN Outside the Given Range