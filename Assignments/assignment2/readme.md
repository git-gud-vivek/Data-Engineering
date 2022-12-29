## Assignment Part-1
__Q1. Why do we call Python as a general purpose and high-level programming language?__
```
=> Because they are not written in machine-readable language, Python programs need to be processed before machines can run them.
Python is an interpreted language. 
That is when a program runs, its interpreter runs through the code and translates it into machine-readable byte code.
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
Type Casting is the method to convert the variable data type into a certain data type in order to the operation required to be performed by users.
There can be two types of Type Casting in Python –

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
```
Strings are arrays of bytes representing Unicode characters.
Strings are immutable, that is we cannot change or delete any character of the string. 
The ways we can declare string in python: 
single_qoute = 'ferrari'
double_qoutes = "lamborghini"
triple_qoutes = ''' big 
                    data''' 
```

__Q27. How can we access the string using its index?__
```
string="iNeuron"
print(string[0]) #i
print(string[-1]) #n
```

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
string = "Big Data iNeuron"
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
```
Lists are just like dynamically sized arrays,and is a sequence data type which is used to store the collection of data. 
List items are ordered, changeable, and allow duplicate values.
A list is a collection of things, enclosed in [ ] and separated by commas.
```

__Q35. How can you create a list in Python?__
``` 
lst = [1,2,'iNeuron',[1,0],(4,8)]
print(lst)
```

__Q36. How can we access the elements in a list?__
```
Using index
lst = [1,2,'iNeuron',[1,0],(4,8)]
print(lst[2]) #iNeuron
```

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
```
A tuple is an immutable collection and are used to store multiple items in a single variable. 
Differences:- 
- Tuples are written with round brackets(), Lists are written with square brackets[]. 
- Tuple are immutable, Lists are mutable. But Both contains ordered and duplicate values.
```

__Q41. How can you create a tuple in Python?__
```
t1 = ('hello',1,(6,2),[7,0],{'key':'value'})
t2 = () #empty tuple
```

__Q42. Create a tuple and try to add your name in the tuple. Are you able to do it? Support your answer with reason.__
```
tupl= (1,2,3)
print(tupl)
We can't add or remove anything from tuple because Tuples are immutable, 
meaning that we cannot change, add or remove items after the tuple has been created.
```

__Q43. Can two tuple be appended. If yes, write a code for it. If not, why?__
```
Yes, 2 tuples can be appended.
t1 = (12, 8, 6)
t2 = (3, 4)
resultTuple = t1 + t2  #Using + operator

resultTuple = sum((t1, t2), ()) #Using sum() func.

l1 = list(t1)        ##Using list() & extend() func.
l2 = list(t2)
l1.extend(l2)
resultTuple = tuple(l1)
print(resultTuple)
```

__Q44. Take a tuple as an input and print the count of elements in it.__
```

```

__Q45. What are sets in Python?__
```
A Set is an unordered collection data type that is iterable, mutable and has no duplicate elements.Set are represented by { }
```

__Q46. How can you create a set?__
```
set1 = set()
set3 = {1}
set2 = {1,3,3,4,6,7,0}
```

__Q47. Create a set and add "iNeuron" in your set.__
```
set1 = {1,3,3,4,67,0}
set1.add("iNeuron")
print(set1)
```

__Q48. Try to add multiple values using add() function.__
```
set1 = set()
set1.add(1)
set1.add(1)
set1.add(2)
set1.add(5)
set1.add(2)
print(set1)
```

__Q49. How is update() different from add()?__
```
- Use add() function to add a single element. Whereas use update() function to add multiple elements to the set.
- add() is faster than update().
- add () accepts immutable parameters only. Whereas update() accepts iterable sequences.
- add() accepts a single parameter, whereas update() can accept multiple sequences.
```

__Q50. What is clear() in sets?__
```
The clear() method removes all elements in a set.
```

__Q51. What is frozen set?__
```
Frozen set is just an immutable version of a Python set object. 
While elements of a set can be modified at any time, elements of the frozen set remain the same after creation.
Due to this, frozen sets can be used as keys in Dictionary or as elements of another set. 
But like sets, it is not ordered (the elements can be set at any index).
Ex:-
vowels = ('a', 'e', 'i', 'o', 'u')
fSet = frozenset(vowels)
```

__Q52. How is frozen set different from set?__
```
Frozen set is just an immutable version of a Python set object. 
While elements of a set can be modified at any time, elements of the frozen set remain the same after creation.
Due to this, frozen sets can be used as keys in Dictionary or as elements of another set. 
But like sets, it is not ordered (the elements can be set at any index).
```

__Q53. What is union() in sets? Explain via code.__
```
union-->returns all the elements from set1 & set2 with no duplicates (set is unordered & unindexed)
set1 = {1,8,0,6,5}
set2 = {1,2,3,5}

setunion = set1 | set2
print(setunion)
```

__Q54. What is intersection() in sets? Explain via code.__
```
#intersection -->retuns all the elements which are common in both sets
set1 = {2,3,4,5,6,2,1}
set2 = {3,4,5,4,9,0}

setintersection = set1 & set2
print(setintersection)
```

__Q55. What is dictionary ibn Python?__
```
A dictionary is a collection of key value pairs which is ordered*, changeable and do not allow duplicates.
```

__Q56. How is dictionary different from all other data structures.__
```
Dictionary items are presented in key:value pairs, and can be referred to by using the key name not by using index. 
Dictionaries cannot have two items with the same key and keys must be immutable.
```

__Q57. How can we delare a dictionary in Python?__
```
dict = {} 
dict1 = {'key1':'heart','key2':4}
print(dict1)
```

__Q58. What will the output of the following?__
```
var = {}
print(type(var)) => Dictionary
```

__Q59. How can we add an element in a dictionary?__
```
dic={}
dic.update({1:"Big"})
dic.update({2:"Data"})
print(dic)
```

__Q60. Create a dictionary and access all the values in that dictionary.__
```
dict2 = {1:'yahoo',2:'gmail',3:'Hotmail'}
values = dict2.values()
print(values)
```

__Q61. Create a nested dictionary and access all the element in the inner dictionary.__
```
Nested_dict = {'a':'apple','b':'brownie','c':'colors','d':{1:1,2:4,3:9}}
print(Nested_dict['d']) ##{1:1,2:4,3:9}
```

__Q62. What is the use of get() function?__
```
Returns the value of the specified key
print(Nested_dict.get('a')) => apple
```

__Q63. What is the use of items() function?__
```
Returns a list containing a tuple for each key value pair
print(Nested_dict.items())
```

__Q64. What is the use of pop() function?__
```
Removes the element with the specified key
print(Nested_dict.pop('b'))
```

__Q65. What is the use of popitems() function?__
```
Removes the last inserted key-value pair
print(Nested_dict.popitem())
```

__Q66. What is the use of keys() function?__
```
Returns a list containing the dictionary's keys
print(Nested_dict.keys())
```

__Q67. What is the use of values() function?__
```
Returns a list of all the values in the dictionary
print(Nestdict.values())
```

__Q68. What are loops in Python?__
```
Loops allows us to execute a statement or block of statements multiple times.
```

__Q69. How many type of loop are there in Python?__
```
There are two types of loops in Python: 
1.While loop 
2.For loop
```

__Q70. What is the difference between for and while loops?__
```
While loops --> A while loop is used to execute a block of statements repeatedly until a given condition is satisfied. 
And when the condition becomes false, the line immediately after the loop in the program is executed. 
sometimes it causes a never ending infinite loop where the condition is always true or if we forget to increment the loop condition explicitly and we have to forcefully terminate the compiler.

for loops -->For loop is used for sequential traversal i.e. it is used for iterating over an iterable like String, Tuple, List, Set or Dictionary.
The indented statements inside the for loops are executed once for each item in an iterable. 
The variable var takes the value of the next item of the iterable each time through the loop and we need not increment it e explicitly.
```

__Q71. What is the use of continue statement?__
```
Continue Statement skips the execution of the program block from after the continue statement and forces the control to start the next iteration. i.e. when the continue statement is executed in the loop, the code inside the loop following the continue statement will be skipped for the current iteration and the next iteration of the loop will begin.
```

__Q72. What is the use of break statement?__
```
Break statement in Python is used to bring the control out of the loop when some external condition is triggered. It terminates the current loop, i.e., the loop in which it appears, and resumes execution at the next statement immediately after the end of that loop.
```

__Q73. What is the use of pass statement?__
```
The pass statement is a null statement.Sometimes, pass is used when the user doesn’t want any code to execute. So user can simply place pass where empty code is not allowed, like in loops, function definitions, class definitions, or in if statements. So using pass statement user avoids this error.
```

__Q74. What is the use of range() function?__
```
The range() function returns a sequence of numbers,in a given range starting from 0 by default,and increments by 1 (by default),and stops before a specified number. The most common use of it is to iterate sequence on a sequence of numbers using Python loops.
```

__Q75. How can you loop over a dictionary?__
```
for k,v in Nestdict.items():
    print(k,v)
```

### Coding problems
__Q76. Write a Python program to find the factorial of a given number.__
```
def fact(num):
     if num==0:
          return 1

     fact_num = num * fact(num-1)
     return fact_num
num=int(input("Enter the number: "))
print(fact(num))
```

__Q77. Write a Python program to calculate the simple interest. Formula to calculate simple interest is SI = (P*R*T)/100__
```
def CalcSI(p,r,t):
    SI = (p*r*t)/100
    return SI

p = int(input("Enter the principal amount:"))
r = float(input("Enter the rate%:"))
t = int(input("Enter the time period:"))

print("Simple Interest is: ", CalcSI(p,r,t))
```

__Q78. Write a Python program to calculate the compound interest. Formula of compound interest is A = P(1+ R/100)^t.__
```
def compound_interest(principle, rate, time):
    Amount = principle * (pow((1 + rate / 100), time))
    CI = Amount - principle
    print("Compound interest is", CI)
 
p = int(input("Enter the principal amount:"))
r = float(input("Enter the rate of interest:"))
t = int(input("Enter the time period:"))
compound_interest(p, r, t)
```

__Q79. Write a Python program to check if a number is prime or not.__
```
import math

n=int(input("Enter any number: "))
count = 0
if n>1:
    for div in range (2,int(math.sqrt(n))+1):
        if (n%div == 0):
            count+=1
            break
    if (count>0):
        print("Given number is not prime")
    else:
        print("Given number is prime")
else:
    print("Given number is not prime")
```

__Q80. Write a Python program to check Armstrong Number.__
```
num = int(input("Enter the number: "))
order = len(str(num))
sum_of_n = 0

temp = num
while temp > 0:
   digit = temp % 10
   sum_of_n += digit ** order
   temp //= 10

if num == sum_of_n:
   print(num,"is an Armstrong number")
else:
   print(num,"is not an Armstrong number")
```

__Q81. Write a Python program to find the n-th Fibonacci Number.__
```
def fibonacci(n):
    if n <= 0:
        return "Incorrect Output"
    data = [0, 1]
    if n > 2:
        for i in range(2, n):
            data.append(data[i-1] + data[i-2])
    return data[n-1]
 
num=int(input("Enter the number: "))
print(fibonacci(num))
```

__Q82. Write a Python program to interchange the first and last element in a list.__
```
def swapList(newList):
    size = len(newList)
    
    temp = newList[0]
    newList[0] = newList[size - 1]
    newList[size - 1] = temp
     
    return newList

newList = [12, 35, 9, 56, 24]
print(swapList(newList))
```

__Q83. Write a Python program to swap two elements in a list.__
```
def swapPositions(list, pos1, pos2):
     
    list[pos1], list[pos2] = list[pos2], list[pos1]
    return list

list = [23, 65, 19, 90]
pos1, pos2  = 1, 3
 
print(swapPositions(list, pos1-1, pos2-1))
```

__Q84. Write a Python program to find N largest element from a list.__
```
def Nmaxelements(list1, N):
    final_list = []
    for i in range(0, N):
        max1 = 0         
        for j in range(len(list1)):    
            if list1[j] > max1:
                max1 = list1[j];
                 
        list1.remove(max1);
        final_list.append(max1)
         
    print(final_list)

list1 = [2, 6, 41, 85, 0, 3, 7, 6, 10]
N = 2
Nmaxelements(list1, N)
```

__Q85. Write a Python program to find cumulative sum of a list.__
```
list=[10,20,30,40,50]
new_list=[]
sum_of_ele=0
for i in range(0,len(list)):
    sum_of_ele+=list[i]
    new_list.append(sum_of_ele)
     
print(new_list)
```

__Q86. Write a Python program to check if a string is palindrome or not.__
```
def isPalindrome(s):
    return s == s[::-1]

s = input("Enter a string: ")
ans = isPalindrome(s)
 
if ans:
    print("Yes")
else:
    print("No")
```

__Q87. Write a Python program to remove i'th element from a string.__
```
def remove(string, i): 
  
    for j in range(len(string)):
        if j == i:
            string = string.replace(string[i], "", 1)
    return string

string = "BigDataiNeuron"
i = 5
print(remove(string, i))
```

__Q88. Write a Python program to check if a substring is present in a given string.__
```
string = "Big data By iNeuron"  
substring = "iNeuron"  

s = string.split()
if substring in s:
    print("yes")
else:
    print("no")
```

__Q89. Write a Python program to find words which are greater than given length k.__
```
n="hello this is big data class by iNeuron"; l=4
s=n.split(" ")
l=list(filter(lambda x: (len(x)>l),s))
print(l)
```

__Q90. Write a Python program to extract unquire dictionary values.__
```
test_dict = {'iNeuron' : [5, 6, 7, 8],
            'is' : [10, 11, 7, 5],
            'best' : [6, 12, 10, 8],
            'for' : [1, 2, 5]}
print("The original dictionary is : " + str(test_dict))

x=[]
for i in test_dict.keys():
    x.extend(test_dict[i])
x=list(set(x))
x.sort()
print("The unique values list is : " + str(x))
```

__Q91. Write a Python program to merge two dictionary.__
```
dict1 = {1:'thread',2:'needle'}
dict2 = {6:'silk',7:'cotton'}

def merge(dict1,dict2):
    res = dict1 | dict2 
    # or return(dict1.update(dict2)) since it returns none
    return res

merge(dict1,dict2)
```

__Q92. Write a Python program to convert a list of tuples into dictionary.__
```
Input : [('Sachin', 10), ('MSD', 7), ('Kohli', 18), ('Rohit', 45)]
Output : {'Sachin': 10, 'MSD': 7, 'Kohli': 18, 'Rohit': 45}
```
```
Input = [('Sachin', 10), ('MSD', 7), ('Kohli', 18), ('Rohit', 45)]

def converter(input):
     result = dict(Input)  
     return result
print(converter(Input))
```

__Q93. Write a Python program to create a list of tuples from given list having number and its cube in each tuple.__
```
Input: list = [9, 5, 6]
Output: [(9, 729), (5, 125), (6, 216)]
```
```
lst = [9, 5, 6]
def createTuple(lst):
    output=[]
    for i in lst:
        tpl = (i,i**3)
        output.append(tpl)
    return output

print(createTuple(lst))
```
__Q94. Write a Python program to get all combinations of 2 tuples.__
```
Input : test_tuple1 = (7, 2), test_tuple2 = (7, 8)
Output : [(7, 7), (7, 8), (2, 7), (2, 8), (7, 7), (7, 2), (8, 7), (8, 2)]
```
```
test_tuple1 = (7, 2)
test_tuple2 = (7, 8)
res =  [(a, b) for a in test_tuple1 for b in test_tuple2]
res = res +  [(a, b) for a in test_tuple2 for b in test_tuple1]

print("The filtered tuple : " + str(res))
```

__Q95. Write a Python program to sort a list of tuples by second item.__
```
Input : [('for', 24), ('Geeks', 8), ('Geeks', 30)] 
Output : [('Geeks', 8), ('for', 24), ('Geeks', 30)]
```
```
def Sort_Tuple(tup):
    lst = len(tup)
    for i in range(0, lst):
        for j in range(0, lst-i-1):
            if (tup[j][1] > tup[j + 1][1]):
                temp = tup[j]
                tup[j]= tup[j + 1]
                tup[j + 1]= temp
    return tup
 
tup =[('for', 24), ('Geeks', 8), ('Geeks', 30)]       
print(Sort_Tuple(tup))
```

__Q96. Write a python program to print below pattern.__
```
* 
* * 
* * * 
* * * * 
* * * * * 
```
```
for i in range(1,6):
    for j in range(1,i+1):
        print("* ",end="")
    print()    
```
__Q97. Write a python program to print below pattern.__
```
    *
   **
  ***
 ****
*****
```
```
sp = 4    #n-1, where n is row
st = 1
for i in range(1,6):
    for j in range(1,sp+1):
        print("  ",end="")
    for j in range(1,st+1):
        print("* ",end="")
    sp-=1
    st+=1
    print()
```

__Q98. Write a python program to print below pattern.__
```
    * 
   * * 
  * * * 
 * * * * 
* * * * * 
```
```
sp = 4 
st = 1
for i in range(1,6):
    for j in range(1,sp+1):
        print("  ",end="")
    for j in range(1,st+1):
        print("*   ",end="")
    sp-=1
    st+=1
    print()
 ```

__Q99. Write a python program to print below pattern.__
```
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```
```
for i in range(1,6):
    num=1
    for j in range(1,i+1):
        print(num ,end=" ")
        num+=1
    print() 
```

Q100. Write a python program to print below pattern.
```
A 
B B 
C C C 
D D D D 
E E E E E 
```
```
ch='A'
for i in range(1,6):
    for j in range(1,i+1):
        print(ch ,end=" ")
    ch=chr(ord(ch)+1)
    print()
```
