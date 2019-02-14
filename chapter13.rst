chapter 13: Object Oriented Programmming
==============================================





13.1 OOP Basic
----------------------------


.. code-block:: python


    #Creat Class Example
    class MyClass:
      x = 05 #Member of MyClass
      y = 10 #Member of MyClass


    my_class_object = MyClass()
    print(my_class_object)           #See what happens when you print object
    print(my_class_object.x)         #This should print x value which is member of MyClass



13.2 Init method
----------------------------


.. code-block:: python

    class Person:
        def __init__(self, name, age):
            self.name = name
            self.age  = age
           # setAge(age)

        def setAge(self,age):
            self.age = age

    person_dagdu = Person("Dagdu", 40)
    print(person_dagdu)
    print("Person Name:" + person_dagdu.name)
    print("Person Age:" + str(person_dagdu.age))


13.3 BuildIn Class Attributes
--------------------------------


.. code-block:: python

    class Person:
        def __init__(self, name, age):
          self.name = name
          self.age = age



    print "Person.__doc__:", Person.__doc__
    print "Person.__name__:", Person.__name__
    print "Person.__module__:", Person.__module__
    print "Person.__bases__:", Person.__bases__
    print "Person.__dict__:", Person.__dict__


13.4 Class And Object
----------------------------


.. code-block:: python

    class Parrot:

        # class attribute
        species = "bird"

        # instance attribute
        def __init__(self, name, age):
            self.name = name
            self.age = age

    # instantiate the Parrot class
    blu = Parrot("Blu", 10)
    woo = Parrot("Woo", 15)

    # access the class attributes
    print("Blu is a {}".format(blu.__class__.species))
    print("Woo is also a {}".format(woo.__class__.species))

    # access the instance attributes
    print("{} is {} years old".format( blu.name, blu.age))
    print("{} is {} years old".format( woo.name, woo.age))



13.5 Encapsulation
----------------------------


.. code-block:: python

    # 1. Using OOP in Python, we can restrict access to methods and variables.
    # 2. This prevent data from direct modification which is called encapsulation.
    # 3. In Python, we denote private attribute using underscore as prefix i.e single "_" or double "__".

    class Computer:

        def __init__(self):
            self.__maxprice = 900

        def sell(self):
            print("Selling Price: {}".format(self.__maxprice))

        def setMaxPrice(self, price):
            self.__maxprice = price

    c = Computer()
    c.sell()

    # change the price
    c.__maxprice = 1000
    c.sell()

    # using setter function
    c.setMaxPrice(1500)
    c.sell()



13.6 Methods
----------------------------


.. code-block:: python

    class Parrot:

        # instance attributes
        def __init__(self, name, age):
            self.name = name
            self.age = age

        # instance method
        def sing(self, song):
            return "{} sings {}".format(self.name, song)

        def dance(self):
            return "{} is now dancing".format(self.name)

    # instantiate the object
    blu = Parrot("Blu", 10)

    # call our instance methods
    print(blu.sing("'Happy'"))
    print(blu.dance())


13.7 Inheritance
----------------------------


.. code-block:: python

    # parent class
    class Bird:

        def __init__(self):
            print("Bird is ready")

        def whoisThis(self):
            print("Bird")

        def swim(self):
            print("Swim faster")

    # child class
    class Penguin(Bird):

        def __init__(self):
            # call super() function
            super().__init__()
            print("Penguin is ready")

        def whoisThis(self):
            print("Penguin")

        def run(self):
            print("Run faster")

    peggy = Penguin()
    peggy.whoisThis()
    peggy.swim()
    peggy.run()

    'In the above program, we created two classes i.e. Bird (parent class) and Penguin (child class).

    The child class inherits the functions of parent class. We can see this from swim() method. Again, the child class modified the behavior of parent class. We can see this from whoisThis() method. Furthermore, we extend the functions of parent class, by creating a new run() method.

    Additionally, we use super() function before __init__() method. This is because we want to pull the content of __init__() method from the parent class into the child class.'


13.8 Polymorphism
----------------------------


.. code-block:: python


    class Parrot:

        def fly(self):
            print("Parrot can fly")

        def swim(self):
            print("Parrot can't swim")

    class Penguin:

        def fly(self):
            print("Penguin can't fly")

        def swim(self):
            print("Penguin can swim")

    # common interface
    def flying_test(bird):
        bird.fly()

    #instantiate objects
    blu = Parrot()
    peggy = Penguin()

    # passing the object
    flying_test(blu)
    flying_test(peggy)

    'In the above program, we defined two classes Parrot and Penguin. Each of them have common method fly() method. However, their functions are different. To allow polymorphism, we created common interface i.e flying_test() function that can take any object. Then, we passed the objects blu and peggy in the flying_test() function, it ran effectively.'



13.9 EmplDepthManagement
----------------------------


.. code-block:: python


    class Employee:
        __id=0
        __name=""
        __gender=""
        __city=""
        __salary=0
        __dept_id=0

        def setEmployeeData(self):
            self.__id = int(input("Enter Id:\t"))
            self.__name = input("Enter Name:\t")
            self.__gender = input("Enter Gender:\t")
            self.__city = input("Enter City:\t")
            self.__salary = int(input("Enter Salary:\t"))
            self.__dept_id = int(input("Enter Department Id:\t"))

        def showEmployeeData(self):
            print("Id\t\t:",self.__id)
            print("Name\t:", self.__name)
            print("Gender\t:", self.__gender)
            print("City\t:", self.__city)
            print("Salary\t:", self.__salary)
            print("Department I\t:",self.__dept_id)


    employees = list(());
    #print(employees)
    print("Enter Employee Details")
    for i in range(1):
        #print(i);
        employee=Employee()
        employee.setEmployeeData()
        employees.append(employee)

    for employee in employees:
        employee.showEmployeeData();

    class Department:
        __id=0
        __name=""
        __emp_count=0

        def setDepartmentData(self):
            self.__id = int(input("Enter Id:\t"))
            self.__name = input("Enter Name:\t")
            self.__emp_count = int(input("Enter Employee Count:\t"))

        def showDepartmentData(self):
            print("Id\t\t:",self.__id)
            print("Name\t\t:", self.__name)
            print("Employee Count\t:",self.__emp_count)

    departments = list(());
    #print(employees)
    print("\n\n Enter Department Details\n")
    for i in range(1):
        #print(i);
        department=Department()
        department.setDepartmentData()
        departments.append(department)

    for department in departments:
        department.showDepartmentData();




Python Programs on Classes and Objects
---------------------------------------------

.. code-block:: python


    Python Program to Find the Area of a Rectangle Using Classes
    Python Program to Append, Delete and Display Elements of a List Using Classes
    Python Program to Find the Area of a Rectangle Using Classes
    Python Program to Create a Class and Compute the Area and the Perimeter of the Circle
    Python Program to Create a Class which Performs Basic Calculator Operations
    Python Program to Create a Class in which One Method Accepts a String from the User and Another Prints it
    Python Program to Create a Class and Get All Possible Subsets from a Set of Distinct Integers