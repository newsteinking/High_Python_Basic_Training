chapter 1: Variables
======================================




1.1 Hello world
----------------------------


.. code-block:: python


    print('Hello World');


1.2 basic variable
----------------------------


.. code-block:: python


    my_first_variable="Yeah, It's a variable";
    print(my_first_variable);




1.3 advance variabe
----------------------------


.. code-block:: python


    x = 4       # x is of type int here
    x = "Sally" # x is now of type str here
    # This is called Dynamic Typing
    #C++ is Static Typing.
    print(x)
    temp = 20
    ferhnite = 27.3+temp
    print(f'Far => {ferhnite}');


1.4 concate output
----------------------------


.. code-block:: python


    my_name = "Sudhir Sapkal";
    print("Hello "+my_name+",Welcome to Python World!!");


1.5 calculate average
----------------------------
Problem Description
The program takes the elements of the list one by one and displays the average of the elements of the list.

Problem Solution
1.	Take the number of elements to be stored in the list as input.
2.	Use a for loop to input elements into the list.
3.	Calculate the total sum of elements in the list.
4.	Divide the sum by total number of elements in the list.
5.	Exit.

.. code-block:: python

    n=int(input("Enter the number of elements to be inserted: "))
    a=[]
    for i in range(0,n):
        elem=int(input("Enter element: "))
        a.append(elem)
    avg=sum(a)/n
    print("Average of elements in the list",round(avg,2))



Program Explanation
1.	User must first enter the number of elements which is stored in the variable n.
2.	The value of I ranges from 0 to the number of elements and is incremented each time after the body of the loop is executed.
3.	Then, the element that the user enters is stored in the variable elem.
4.	a.append(elem) appends the element to the list.
5.	Now the value of i is incremented to 2.
6.	The new value entered by the user for the next loop iteration is now stored in elem which is appended to the list.
7.	The loop runs till the value of i reaches n.
8.	sum(a) gives the total sum of all the elements in the list and dividing it by the total number of elements gives the average of elements in the list.
9.	round(avg,2) rounds the average upto 2 decimal places.
10.	Then the average is printed after rounding.


1.6 exchange variables
----------------------------
Problem Description
The program takes both the values from the user and swaps them without using temporary variable.

Problem Solution
1.	Take the values of both the elements from the user.
2.	Store the values in separate variables.
3.	Add both the variables and store it in the first variable.
4.	Subtract the second variable from the first and store it in the second variable.
5.	Then, subtract the first variable from the second variable and store it in the first variable.
6.	Print the swapped values.
7.	Exit.


.. code-block:: python

    a=int(input("Enter value of first variable: "))
    b=int(input("Enter value of second variable: "))
    a=a+b
    b=a-b
    a=a-b
    print("a is:",a," b is:",b)


Program Explanation
1.	User must first enter the values for both the elements.
2.	The first element is assigned the sum of the first two elements.
3.	Second element is assigned the difference between the sum in the first variable and the second variable, which is basically the first element.
4.	Later the first element is assigned the difference between the sum in the variable and the second variable, which is the second element.
5.	Then the swapped values are printed.





1.7 number n nm
----------------------------
Problem Description
The program takes a number n and computes n+nn+nnn.

Problem Solution
1.	Take the value of a element and store in a variable n.
2.	Convert the integer into string and store it in another variable.
3.	Add the string twice so the string gets concatenated and store it in another variable.
4.	Then add the string thrice and assign the value to the third variable.
5.	Convert the strings in the second and third variables into integers.
6.	Add the values in all the integers.
7.	Print the total value of the expression.
8.	Exit.


.. code-block:: python


    n=int(input("Enter a number n: "))
    temp=str(n)
    t1=temp+temp
    t2=temp+temp+temp
    comp=n+int(t1)+int(t2)
    print("The value is:",comp)


Program Explanation
1.	User must first enter the value and store it in a variable n.
2.	The integer is converted to string for concatenation of the value of n.
3.	The string is then concatenated once and twice and stored in separate variables.
4.	Later to find the total sum, the string is converted back to integer.
5.	The total value of the expression is then printed.




1.4 concate output
----------------------------

.. code-block:: python


1.4 concate output
----------------------------


.. code-block:: python