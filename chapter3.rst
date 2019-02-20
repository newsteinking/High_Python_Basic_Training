chapter 3: Operators
==============================================



3.1 airthmatic
----------------------------


.. code-block:: python


    x = 5;
    y = 2;
    addi  = x+y;
    subs  = x-y;
    mult = x*y;
    div  = x/y;
    mod  = x%y;
    expo = x**y;
    floordiv = x//y;
    print(f'Add {addi}');
    print(f'Sub {subs}');
    print(f'Mult {mult}');
    print(f'Div {div}');
    print(f'Mod {mod}');
    print(f'expo {expo}');
    print(f'Floor Div {floordiv}');




3.2 special operatorr
----------------------------


.. code-block:: python


    #1. Identity Operator
    x1 = 5
    y1 = 5
    x2 = 'Hello'
    y2 = 'Hello'
    x3 = [1,2,3]
    y3 = [1,2,3]

    # Output: False
    print(x1 is not y1)

    # Output: True
    print(x2 is y2)

    # Output: False
    print(x3 is y3)

    #2. Membership operator
    x = 'Hello world'
    y = {1:'a',2:'b'}

    # Output: True
    print('H' in x)

    # Output: True
    print('hello' not in x)

    # Output: True
    print(1 in y)

    # Output: False
    print('a' in y)

