chapter 0: Variables
======================================




0.1 Hello world
----------------------------


.. code-block:: python


    print('Hello World');


0.2 basic variable
----------------------------


.. code-block:: python


    my_first_variable="Yeah, It's a variable";
    print(my_first_variable);




0.3 advance variabe
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


0.4 concate output
----------------------------


.. code-block:: python


    my_name = "Sudhir Sapkal";
    print("Hello "+my_name+",Welcome to Python World!!");


Simple Python Programs
-------------------------------------------------------------


.. code-block:: python


    Python Program to Calculate the Average of Numbers in a Given List
    Python Program to Exchange the Values of Two Numbers Without Using a Temporary Variable
    Python Program to Read a Mumber n and Compute n+nn+nnn
    Python Program to Reverse a Given Number
    Python Program to Check Whether a Number is Positive or Negative
    Python Program to Take in the Marks of 5 Subjects and Display the Grade
    Python Program to Print all Numbers in a Range Divisible by a Given Number
    Python Program to Read Two Numbers and Print Their Quotient and Remainder
    Python Program to Accept Three Digits and Print all Possible Combinations from the Digits
    Python Program to Print Odd Numbers Within a Given Range
    Python Program to Find the Sum of Digits in a Number
    Python Program to Find the Smallest Divisor of an Integer
    Python Program to Count the Number of Digits in a Number
    Python Program to Check if a Number is a Palindrome
    Python Program to Print all Integers that Aren't Divisible by Either 2 or 3 and Lie between 1 and 50.
    Python Program to Read a Number n And Print the Series "1+2+…..+n= "
    Python Program to Read a Number n and Print the Natural Numbers Summation Pattern
    Python Program to Print an Identity Matrix
    Python Program to Print an Inverted Star Pattern
    Python Program to Read Print Prime Numbers in a Range using Sieve of Eratosthenes


Vanya and Fence
-------------------------------------------------------------
http://codeforces.com/problemset/problem/677/A

친구들이 같이 담 옆을 걸어가고자 한다. 그런데 집주인한테 보이지 않게 하기 위해서
담보다 큰 친구들은 허리를 굽혀서 걸어가야 한다.
담보다 작은 친구는 1폭을 걸어간다고 하고 굽혀서 가는 친구들은 0.5폭씩 가야한다고 할때
친구수와 담 높이가 주어지고 친구들의 키가 주어질때  모든 친구들이 한폭을 갈수 있는 최소 거리는 어떻게 되는가?

inputCopy
3(사람수) 7(펜수높이)
4 5 14
outputCopy
4
inputCopy
6 1
1 1 1 1 1 1
outputCopy
6
inputCopy
6 5
7 6 8 9 10 5
outputCopy
11

Input :   n - 사람 수      h - 펜스의 높이

  a_1, a_2 ....a_n - 사람의 키



Output : 키와 펜스 비교하여 합연산

  키 <= 펜스   : 1

  키  >  펜스   : 2



예제 해석 :  n = 3, h = 7

       a_1 = 4, a_2 = 5, a_3 = 14



       4 <= 7 ----------1

       5 <= 7 ----------1

       14 > 7 ----------2



       따라서

       1,1,2 를 합연산하여 Output은 4가 됩니다.

.. code-block:: python


    def cal_road_width(_a, _h):
        road_width = 0
        for ai in _a:
            road_width += 1 if ai <= _h else 2

        return road_width

    n, h = map(int, input("").split())
    a = list(map(int, input().split()))
    print(cal_road_width(a, h))


Simple Python Programs
-------------------------------------------------------------