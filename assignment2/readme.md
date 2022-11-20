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


__Q26. What is a string? How can we declare string in Python?__

__Q27. How can we access the string using its index?__

__Q28. Write a code to get the desired output of the following__
```
string = "Big Data iNeuron"
desired_output = "iNeuron"
```
```
string = "Big Data iNeuron"
temp = list(string.split())
print(temp[2])
```

__Q29. Write a code to get the desired output of the following__
```
string = "Big Data iNeuron"
desired_output = "norueNi"
```
```
string = "Big Data iNeuron"
temp = list(string[::-1].split())
print(temp[0])
```

__Q30. Resverse the string given in the above question.__
```
print(string[::-1])
```
__Q31. How can you delete entire string at once?__
```
print(string.replace("Big Data iNeuron", "")) 
or
del string
```

__Q32. What is escape sequence?__
```
An escape sequence is a sequence of characters that, when used inside a character or string, does not represent itself but is converted into another character or series of characters. ex :- \', \", \\,\n etc
```

__Q33. How can you print the below string?__
```
'iNeuron's Big Data Course'
```
```
print('iNeuron\'s Big Data Course')
```

__Q34. What is a list in Python?__

__Q35. How can you create a list in Python?__

__Q36. How can we access the elements in a list?__

__Q37. Write a code to access the word "iNeuron" from the given list.__
```
lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
``` 
```
print(lst[4][2])
```

__Q38. Take a list as an input from the user and find the length of the list.__
```
try:
    lst = []
    while True:
        lst.append(int(input()))
except:
    print("Size of list is: ",len(lst))
```

__Q39. Add the word "Big" in the 3rd index of the given list.__
```
lst = ["Welcome", "to", "Data", "course"]
```
```
lst = ["Welcome", "to", "Data", "course"]
lst.insert(2, "Big")
print(lst)
```

__Q40. What is a tuple? How is it different from list?__

__Q41. How can you create a tuple in Python?__

__Q42. Create a tuple and try to add your name in the tuple. Are you able to do it? Support your answer with reason.__

__Q43. Can two tuple be appended. If yes, write a code for it. If not, why?__

__Q44. Take a tuple as an input and print the count of elements in it.__

__Q45. What are sets in Python?__

__Q46. How can you create a set?__

__Q47. Create a set and add "iNeuron" in your set.__

__Q48. Try to add multiple values using add() function.__

__Q49. How is update() different from add()?__

__Q50. What is clear() in sets?__

__Q51. What is frozen set?__

__Q52. How is frozen set different from set?__

__Q53. What is union() in sets? Explain via code.__

__Q54. What is intersection() in sets? Explain via code.__

__Q55. What is dictionary ibn Python?__

__Q56. How is dictionary different from all other data structures.__

__Q57. How can we delare a dictionary in Python?__

__Q58. What will the output of the following?__
```
var = {}
print(type(var)) ##Dictionary
```

__Q59. How can we add an element in a dictionary?__

__Q60. Create a dictionary and access all the values in that dictionary.__

__Q61. Create a nested dictionary and access all the element in the inner dictionary.__

__Q62. What is the use of get() function?__

__Q63. What is the use of items() function?__

__Q64. What is the use of pop() function?__

__Q65. What is the use of popitems() function?__

__Q66. What is the use of keys() function?__

__Q67. What is the use of values() function?__

__Q68. What are loops in Python?__

__Q69. How many type of loop are there in Python?__

__Q70. What is the difference between for and while loops?__

__Q71. What is the use of continue statement?__

__Q72. What is the use of break statement?__

__Q73. What is the use of pass statement?__

__Q74. What is the use of range() function?__

__Q75. How can you loop over a dictionary?__


### Coding problems
Q76. Write a Python program to find the factorial of a given number.

Q77. Write a Python program to calculate the simple interest. Formula to calculate simple interest is SI = (P*R*T)/100

Q78. Write a Python program to calculate the compound interest. Formula of compound interest is A = P(1+ R/100)^t.

Q79. Write a Python program to check if a number is prime or not.

Q80. Write a Python program to check Armstrong Number.

Q81. Write a Python program to find the n-th Fibonacci Number.

Q82. Write a Python program to interchange the first and last element in a list.

Q83. Write a Python program to swap two elements in a list.

Q84. Write a Python program to find N largest element from a list.

Q85. Write a Python program to find cumulative sum of a list.

Q86. Write a Python program to check if a string is palindrome or not.

Q87. Write a Python program to remove i'th element from a string.

Q88. Write a Python program to check if a substring is present in a given string.

Q89. Write a Python program to find words which are greater than given length k.

Q90. Write a Python program to extract unquire dictionary values.

Q91. Write a Python program to merge two dictionary.

Q92. Write a Python program to convert a list of tuples into dictionary.
```
Input : [('Sachin', 10), ('MSD', 7), ('Kohli', 18), ('Rohit', 45)]
Output : {'Sachin': 10, 'MSD': 7, 'Kohli': 18, 'Rohit': 45}
```

Q93. Write a Python program to create a list of tuples from given list having number and its cube in each tuple.
```
Input: list = [9, 5, 6]
Output: [(9, 729), (5, 125), (6, 216)]
```

Q94. Write a Python program to get all combinations of 2 tuples.
```
Input : test_tuple1 = (7, 2), test_tuple2 = (7, 8)
Output : [(7, 7), (7, 8), (2, 7), (2, 8), (7, 7), (7, 2), (8, 7), (8, 2)]
```

Q95. Write a Python program to sort a list of tuples by second item.
```
Input : [('for', 24), ('Geeks', 8), ('Geeks', 30)] 
Output : [('Geeks', 8), ('for', 24), ('Geeks', 30)]
```

Q96. Write a python program to print below pattern.
```
* 
* * 
* * * 
* * * * 
* * * * * 
```
Q97. Write a python program to print below pattern.
```
    *
   **
  ***
 ****
*****
```

Q98. Write a python program to print below pattern.
```
    * 
   * * 
  * * * 
 * * * * 
* * * * * 
```

Q99. Write a python program to print below pattern.
```
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```

Q100. Write a python program to print below pattern.
```
A 
B B 
C C C 
D D D D 
E E E E E 
```
