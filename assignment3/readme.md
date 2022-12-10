## Python OOP Assignment

__Q1. What is the purpose of Python's OOP?__
```
The main purpose of OOPs is to bind the data and the functions that work on that together as a single unit so that no other part of the code can access this data.
OOP concepts are:-
-class
-object
-Polymorphism
-Inheritance
-Encapsulation
-Data abstraction
```

__Q2. Where does an inheritance search look for an attribute?__
```
 An inheritance search looks for an attribute first in the instance object, 
 then in the class the instance was created from, then in all higher superclasses, progressing from left to right (by default). 
 The search stops at the first place the attribute is found.
```

__Q3. How do you distinguish between a class object and an instance object?__
```
Class objects/variables are declared inside a class but outside of any function. Instance objects/variables are declared inside the constructor which is the __init__method.

class Book():
   fontsize = 9
   page_width = 15
   def __init__(self, name, writer, length):
      self.name = name
      self.writer = writer
      self.length = length

fontsize & page_width are class object
name, writer & length are instance object.
```

__Q4. What makes the first argument in a class’s method function special?__
```
When we define a class in Python, every method that we define, must accept instance of that class as its first argument (called self by convention).
The self variable points to the instance of the class that we're working with.
```

__Q5. What is the purpose of the init method?__
```
The __init__ method lets the class initialize the object's attributes and serves no other purpose. It is only used within classes.

Constructors are used to initializing the object’s state. The task of constructors is to initialize(assign values) to the data members of the class when an object of the class is created. Like methods, a constructor also contains a collection of statements(i.e. instructions) that are executed at the time of Object creation. It is run as soon as an object of a class is instantiated. The method is useful to do any initialization we want to do with our object.
```
__Q6. What is the process for creating a class instance?__
```
class Employee:
   'Common base class for all employees'
   empCount = 0

   def __init__(self, name, salary):
      self.name = name
      self.salary = salary
      Employee.empCount += 1

To create instances of a class, we call the class using class name and pass in whatever arguments its __init__ method accepts.
emp1 = Employee("Zara", 2000)
emp2 = Employee("Manni", 5000)
```

__Q7. What is the process for creating a class?__
```
The class statement creates a new class definition. The name of the class immediately follows the keyword class followed by a colon as follows −
class Employee:
   'Common base class for all employees'
   empCount = 0

   def __init__(self, name, salary):
      self.name = name
      self.salary = salary
      Employee.empCount += 1
```

__Q8. How would you define the superclasses of a class?__
```
The class from which a class inherits is called the parent or superclass. A class which inherits from a superclass is called a subclass, also called heir class or child class.
class Robot:
    def __init__(self, name):
        self.name = name
    def say_hi(self):
        print("Hi, I am " + self.name)
class PhysicianRobot(Robot):
    pass
x = Robot("Marvin")
y = PhysicianRobot("James")
print(x, type(x))
print(y, type(y))
y.say_hi()
```

__Q9. What is the relationship between classes and modules?__
```
A module in python is simply a way to organize the code, and it contains either python classes or just functions. If we need those classes or functions in our project, we just import them. For instance, the math module in python contains just a bunch of functions, and we just call those needed (math.pow).

On the other hand a python class is something similar to a java class, it's only structured in a slightly different way.
```

__Q10. How do you make instances and classes?__
```
Creating class-

class Employee:
   'Common base class for all employees'
   empCount = 0

   def __init__(self, name, salary):
      self.name = name
      self.salary = salary
      Employee.empCount += 1

To create instances of a class, we call the class using class name and pass in whatever arguments its __init__ method accepts.
emp1 = Employee("Zara", 2000)
emp2 = Employee("Manni", 5000)
```

__Q11. Where and how should be class attributes created?__
```
class Employee:
   'Common base class for all employees'
   empCount = 0 // class attribute

   def __init__(self, name, salary):
      self.name = name   //instance attribute
      self.salary = salary   //instance attribute
      Employee.empCount += 1
```

__Q12. Where and how are instance attributes created?__
```
class Employee:
   'Common base class for all employees'
   empCount = 0 // class attribute

   def __init__(self, name, salary):
      self.name = name   //instance attribute
      self.salary = salary   //instance attribute
      Employee.empCount += 1
```

__Q13. What does the term "self" in a Python class mean?__
```
When we define a class in Python, every method that we define, must accept instance of that class as its first argument (called self by convention).
The self variable points to the instance of the class that we're working with.
```

__Q14. How does a Python class handle operator overloading?__
```
When we use an operator on user-defined data types then automatically a special function or magic function associated with that operator is invoked. Changing the behavior of operator is as simple as changing the behavior of a method or function. that is, When we use + operator, the magic method __add__ is automatically invoked in which the operation for + operator is defined. Thereby changing this magic method’s code, we can give extra meaning to the + operator. 
Ex1:-
class A:
    def __init__(self, a):
        self.a = a
 
    # adding two objects
    def __add__(self, o):
        return self.a + o.a
ob1 = A(1)
ob2 = A(2)
ob3 = A("Geeks")
ob4 = A("For")
 
print(ob1 + ob2)
print(ob3 + ob4)
# Actual working when Binary Operator is used.
print(A.__add__(ob1 , ob2))
print(A.__add__(ob3,ob4))
#And can also be Understand as :
print(ob1.__add__(ob2))
print(ob3.__add__(ob4))

Ex2:-
class complex:
    def __init__(self, a, b):
        self.a = a
        self.b = b
 
     # adding two objects
    def __add__(self, other):
        return self.a + other.a, self.b + other.b
 
Ob1 = complex(1, 2)
Ob2 = complex(2, 3)
Ob3 = Ob1 + Ob2
print(Ob3)
```

__Q15. When do you consider allowing operator overloading of your classes?__
```
Operator Overloading means giving extended meaning beyond their predefined operational meaning.

Consider that we have two objects which are a physical representation of a class (user-defined data type) and we have to add two objects with binary ‘+’ operator it throws an error, because compiler don’t know how to add two objects. So we define a method for an operator and that process is called operator overloading.

class complex:
    def __init__(self, a, b):
        self.a = a
        self.b = b
 
     # adding two objects
    def __add__(self, other):
        return self.a + other.a, self.b + other.b
 
Ob1 = complex(1, 2)
Ob2 = complex(2, 3)
Ob3 = Ob1 + Ob2
print(Ob3) //output = (3,5)
```

__Q16. What is the most popular form of operator overloading?__
```

```

__Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?__
```
Inheritance and Polymorphism. 
```

__Q18. Describe three applications for exception processing.__
```

```

__Q19. What happens if you don't do something extra to treat an exception?__
```

```

__Q20. What are your options for recovering from an exception in your script?__
```

```

__Q21. Describe two methods for triggering exceptions in your script.__
```

```

__Q22. Identify two methods for specifying actions to be executed at termination time, regardless of whether or not an exception exists.__
```

```

__Q23. What is the purpose of the try statement?__
```

```

__Q24. What are the two most popular try statement variations?__
```

```

__Q25. What is the purpose of the raise statement?__
```

```

__Q26. What does the assert statement do, and what other statement is it like?__
```

```

__Q27. What is the purpose of the with/as argument, and what other statement is it like?__
```

```

__Q28. What are *args, **kwargs?__
```

```

__Q29. How can I pass optional or keyword parameters from one function to another?__
```

```

__Q30. What are Lambda Functions?__
```

```

__Q31. Explain Inheritance in Python with an example?__
```

```

__Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of class C, which version gets invoked?__
```

```

__Q33. Which methods/functions do we use to determine the type of instance and inheritance?__
```

```

__Q34.Explain the use of the 'nonlocal' keyword in Python.__
```

```

__Q35. What is the global keyword?__
```

```
