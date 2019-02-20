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
담보다 작은 친구는 1길이만큼 을 걸어간다고 하고 굽혀서 가는 친구들은 2 길이만큼  갈 수 있다고  할때
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


Water Buying
-------------------------------------------------------------

http://codeforces.com/problemset/problem/510/A

A. Fox And Snake
time limit per test2 seconds
memory limit per test256 megabytes
inputstandard input
outputstandard output
Fox Ciel starts to learn programming. The first task is drawing a fox! However, t
hat turns out to be too hard for a beginner, so she decides to draw a snake instead.

A snake is a pattern on a n by m table. Denote c-th cell of r-th row as (r, c).
The tail of the snake is located at (1, 1), then it's body extends to (1, m),
then goes down 2 rows to (3, m), then goes left to (3, 1) and so on.

Your task is to draw this snake for Fox Ciel: the empty cells should be represented as dot characters ('.')
and the snake cells should be filled with number signs ('#').

Consider sample tests in order to understand the snake pattern.

Input
The only line contains two integers: n and m (3 ≤ n, m ≤ 50).

n is an odd number.

Output
Output n lines. Each line should contain a string consisting of m characters. Do not output spaces.

Examples
inputCopy
3 3
outputCopy
###
..#
###
inputCopy
3 4
outputCopy
####
...#
####
inputCopy
5 3
outputCopy
###
..#
###
#..
###
inputCopy
9 9
outputCopy
#########
........#
#########
#........
#########
........#
#########
#........
#########

첫수가 홀수이고 두 수를 입력하면 위에서 처럼 뱀꼬리 연결하듯이 효현을 하는것이다.
두 수 n,m을 입력하면 (n,m) 이 만들어지고 초기 (1,1)에서 시작해서 (1,m)으로 끝나고 #이 입력되고
다음 라인은 (3,m)-->(3,1) 로 가는 구조이다. 뱀을 연결하기 위해 # 이 사용되고
빈공간은 . 로 표기된다.

.. code-block:: python


    n, m = map(int, input().split())
    for i in range(n):
        if i % 2 == 0:
            print("#"*m)
        else:
            s = ["."]*m
            s[(i//2)%2-1] = "#"
            print("".join(s))
