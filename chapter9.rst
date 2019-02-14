chapter 9: Files
=========================================


9.1 File
----------------------------


.. code-block:: python


    f = open("demo.txt", "r")
    #print(f.read())

    #Read Only Parts of the File
    #By default the read() method returns the whole text, but you can also specify how many character you want to return:

    #print(f.read(5))

    #Read Lines
    #You can return one line by using the readline() method:
    print(f.readline())


    demo.txt
    Hello! Welcome to demo.txt
    This file is for testing purposes.
    Good Luck!

Python Programs on File Handling
-----------------------------------

.. code-block:: python

    Python Program to Read the Contents of a File
    Python Program to Count the Number of Words in a Text File
    Python Program to Count the Number of Lines in a Text File
    Python Program to Read a String from the User and Append it into a File
    Python Program to Count the Occurrences of a Word in a Text File
    Python Program to Copy the Contents of One File into Another
    Python Program that Reads a Text File and Counts the Number of Times a Certain Letter Appears in the Text File
    Python Program to Read a Text File and Print all the Numbers Present in the Text File
    Python Program to Append the Contents of One File to Another File
    Python Program to Count the Number of Blank Spaces in a Text File
    Python Program to Read a File and Capitalize the First Letter of Every Word in the File
    Python Program to Read the Contents of a File in Reverse Order