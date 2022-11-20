## Assignment Part-1
__Q1. Why do we call Python as a general purpose and high-level programming language?__
```
=> Because they are not written in machine-readable language, Python programs need to be processed before machines can run them. Python is an interpreted    language. That is when a program runs, its interpreter runs through the code and translates it into machine-readable byte code.
```
__Q2. Why is Python called a dynamically typed language?__
```
=> Because the type of the variable is determined only during runtime.
```
__Q3. List some pros and cons of Python programming language?__
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
__Q4. In what all domains can we use Python?__
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
__Q5. What are variable and how can we declare them?__
```
Variables are containers for storing data values.
Python has no command for declaring a variable.A variable is created the moment you first assign a value to it.
ex:- x=5, var= "vivek", etc.
```
__Q6. How can we take an input from the user in Python?__
```
Using input() function.
```
__Q7. What is the default datatype of the value that has been taken as an input using input() function?__
```
String 
```
__Q8. What is type casting?__
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
__Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?__
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
# Taking multiple inputs in a single line and type casting using list() function  
x = list(map(int, input("Enter multiple values: ").split()))  
print("List of students: ", x) 
```

__Q10. What are keywords?__
```
Keywords are special reserved words that have specific meanings and purposes and can't be used for anything but those specific purposes.
Ex- for, while, finally, from, False, True, etc.
```

__Q11. Can we use keywords as a variable? Support your answer with reason.__
```
No, because it will create dilemma for interpreter.
```

__Q12. What is indentation? What's the use of indentaion in Python?__
```
Python indentation refers to adding white space before a statement to a particular block of code. In another word, all the statements with the same space to the right, belong to the same block.
```
<img width="480" alt="Screenshot 2022-11-20 at 10 10 20 AM" src="https://user-images.githubusercontent.com/118146044/202885935-fb85198e-e894-408c-bc0b-daa78db91fb2.png">

__Q13. How can we throw some output in Python?__

__Q14. What are operators in Python?__
```
Operators are special symbols that perform operations on variables and values. For example,
print(5 + 6)   # 11
-Types of operators:-
   - Arithmetic (+,-,*,/,%,**)
   - Assignment (=,+=,-=,*=,/=,%=,**=)
   - Comparison (==, <=, >=, !=, <, >)
   - Logical (and, or, not)
   - Bitwise (&, |, -, ^, >>)
   - Special (Identity op(is, is not), Membership op(in, not in))
```

__Q15. What is difference between / and // operators?__
```
/ => Float division
// => Integer divison
```
__Q16. Write a code that gives following as an output.__
```
iNeuroniNeuroniNeuroniNeuron
```
```
Solution:-
for i in range(1,5):
    print("iNeuron", end="")
```

__Q17. Write a code to take a number as an input from the user and check if the number is odd or even.__
```
var = int(input("Enter a number: "))
if var > 0:
    if var%2 == 0:
        print ("Given number is even")
    else:
        print ("Given number is odd")
else: 
    print ("Give valid  positive number")
```

__Q18. What are boolean operator?__
```
Boolean operators are Logical operators(and, or, not)
```

__Q19. What will the output of the following?__
```
1 or 0  => 1

0 and 0  => 0

True and False and True  => false

1 or 0 or 0  => 1
```

__Q20. What are conditional statements in Python?__
```
if , else, elif
```

__Q21. What is use of 'if', 'elif' and 'else' keywords?__
```
To check for particular conditions and run the program accordingly.
```

__Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".__
```
var = int(input("Enter your age: "))
if var>=18:
    print ("I can vote")
else:
    print ("I can't vote")
```

__Q23. Write a code that displays the sum of all the even numbers from the given list.__
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
```
numbers = [12, 75, 150, 180, 145, 525, 50]
sum_of_even = 0 
for num in numbers:
    if num%2 == 0:
        sum_of_even += num

print(sum_of_even)  
```
__Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.__
```
x,y,z =input("Enter 3 number: ").split()
x = int(x)
y = int(y)
z = int(z)

if x>y and x>z:
    print("greatest number: ", x)
elif y>x and y>z:
    print("greatest number: ", y)
elif z>x and z>y:
    print("greatest number: ", z)

```

__Q25. Write a program to display only those numbers from a list that satisfy the following conditions__

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
```
numbers = [12, 75, 150, 180, 145, 525, 50]
display = []
for num in numbers:
    if num%5==0 and num<150:
        display.append(num)
    elif num>500:
        break
print(display)
```
