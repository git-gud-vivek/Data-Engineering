## Assignment Part-1
Q1. Why do we call Python as a general purpose and high-level programming language?
```
=> Because they are not written in machine-readable language, Python programs need to be processed before machines can run them. Python is an interpreted    language. That is when a program runs, its interpreter runs through the code and translates it into machine-readable byte code.
```
Q2. Why is Python called a dynamically typed language?
```
=> Because the type of the variable is determined only during runtime.
```
Q3. List some pros and cons of Python programming language?
```
1. Pros:-
   - It's Simple.
   - It's Free.
   - It's Easy to Use.
   - It's Highly Compatible.
   - It is Object-Oriented.
   - It has Lots of Libraries.
   - It has Built-in Data Structures.
   - It's Widely Applicable. 
2. Cons:-
   - Poor memory efficiency.
   - Slow speed
   - Underdeveloped Database access layer compared to ODBC.
   - Weak in mobile computing
   - Runtime errors.
```
Q4. In what all domains can we use Python?
```
Domains where we can use python:-
- Data Science
- Automation
- Application Devlopment
- AI & ML
- Desktop GUI
- Audio/ video application
- Console application
```
Q5. What are variable and how can we declare them?
```
Variables are containers for storing data values.
Python has no command for declaring a variable.A variable is created the moment you first assign a value to it.
ex:- x=5, var= "vivek", etc.
```

Q6. How can we take an input from the user in Python?
```
Using input() function.
```

Q7. What is the default datatype of the value that has been taken as an input using input() function?
```
String 
```

Q8. What is type casting?
```
Type Casting is the method to convert the variable data type into a certain data type in order to the operation required to be performed by users. In this article, we will see the various technique for typecasting.There can be two types of Type Casting in Python –

1. Implicit Type Casting:-
  a = 7
  b = 3.0
# Python automatically converts
# c to float as it is a float addition
  c = a + b
  print(c)
  print(type(c))
2. Explicit Type Casting:-
  x = int(1)   # x will be 1
  y = int(2.8) # y will be 2
  z = int("3") # z will be 3
  
  x = float(1)     # x will be 1.0
  y = float(2.8)   # y will be 2.8
  z = float("3")   # z will be 3.0
  w = float("4.2") # w will be 4.2
  
  x = str("s1") # x will be 's1'
  y = str(2)    # y will be '2'
  z = str(3.0)  # z will be '3.0'
```

Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?
```
Yes,
Using split() Method. The split() method is useful for getting multiple inputs from users.
**input().split(separator, maxsplit)**
Ex- 
x, y, z = input("Enter three values: ").split()  
print("Total number of students: ", x)  
print("Number of passed student : ", y)  
print("Number of failed student : ", z)  

We can also take values and convert them into the list using the map() method along with the split() method.
```# Taking multiple inputs in a single line and type casting using list() function  
x = list(map(int, input("Enter multiple values: ").split()))  
print("List of students: ", x) ``` 
```

Q10. What are keywords?
```
Keywords are special reserved words that have specific meanings and purposes and can't be used for anything but those specific purposes.
Ex- for, while, finally, from, False, True, etc.
```

Q11. Can we use keywords as a variable? Support your answer with reason.
```
No, because it will create dilemma for interpreter.
```

Q12. What is indentation? What's the use of indentaion in Python?
```
Python indentation refers to adding white space before a statement to a particular block of code. In another word, all the statements with the same space to the right, belong to the same block.
[![image from gfg](/assets/images/ex.jpg "example")](https://media.geeksforgeeks.org/wp-content/uploads/20191125112615/Indentation-python2.jpg)
```

Q13. How can we throw some output in Python?

Q14. What are operators in Python?

Q15. What is difference between / and // operators?

Q16. Write a code that gives following as an output.
```
iNeuroniNeuroniNeuroniNeuron
```
```
Solution:-
for i in range(1,5):
    print("iNeuron", end="")
```

Q17. Write a code to take a number as an input from the user and check if the number is odd or even.

Q18. What are boolean operator?

Q19. What will the output of the following?
```
1 or 0  => 1

0 and 0  => 0

True and False and True  => false

1 or 0 or 0  => 1
```

Q20. What are conditional statements in Python?

Q21. What is use of 'if', 'elif' and 'else' keywords?

Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".

Q23. Write a code that displays the sum of all the even numbers from the given list.
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```


Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.

Q25. Write a program to display only those numbers from a list that satisfy the following conditions

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
