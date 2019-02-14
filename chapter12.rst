chapter 12: Method And Functions
==================================




12.1 args AND kargs
----------------------------


.. code-block:: python

    def myfunc(*args):
        return sum(args) * 0.05

    print(myfunc(50,60))

    #args - python treats agrs as tuples
    #args is just name , it can be anything , just make sure it should followed with '*' symbol

    def myfuncforkargs(**kwargs):
        print(kwargs)
        if 'fruit' in kwargs:
            print('My fruit of choice is {}'.format(kwargs['fruit']))
        else:
            print('I did not find any fruit here')

    myfuncforkargs(fruit="apple",icecream="butterscotch")

    #kargs - means it is sending the argubments as key word arguments called as dictonories

    #we can use both at same time

    def my_function(*args,**kwargs):
        print('I would like {} {}'.format(args[0],kwargs['food']))

    my_function(10,20,30,food="eggs",fruit="apple")



12.2 My Function
----------------------------


.. code-block:: python


    #Example
    #Creating a function

    def my_function():
      print("Hello from a function")

    #Calling a Function
    my_function()

    #How to send parameters
    def greetings(name):
        print("Good Morning, "+name)

    #Calling a greetings function
    greetings("Vinay")

    #Returning function
    def addition(num1,num2):
        return num1+num2;

    #Calling addition function
    #print("Addition =>"+addition(10,20)) #Will give error
    result = addition(10,20)
    print("Addition of 10 and 20 is {}".format(result))

    #Default Parameter Value
    #The following example shows how to use a default parameter value.
    #If we call the function without parameter, it uses the default value:

    def substraction(num1=0,num2=0):
        print(num1-num2)

    substraction(30,20)
    substraction();
    substraction(50,50)



12.3 neted statement And Scope
---------------------------------


.. code-block:: python

    x = 20
    def printer():
        x=10
        return x

    print(x)

    #LEGB
    #1. Local(L): Defined inside function/class
    #2. Enclosed(E): Defined inside enclosing functions(Nested function concept)
    #3. Global(G): Defined at the uppermost level
    #4. Built-in(B): Reserved names in Python builtin modules

    #Globle
    name = "Global Sudhir"

    def greet():

        #ENCLOSING
        name = "Enclosing Sudhir"

        def hello():
            #LOCAL
            name = "LOCAL Sudhir"
            print("Hello "+name)

        hello()

    greet()





12.4 pig latin
----------------------------


.. code-block:: python


    def pig_latin(word):
        first_letter = word[0];

        if first_letter in 'aeiou':
            pig_word = word + 'ay';
        else:
            pig_word = word[1:] + first_letter + 'ey'

        return pig_word;

    print(pig_latin('apple'));