# Python notes
---
# Getting Started
---
### What is Python
+ The world's fastest growing and most popular programming language among: Software Engineers, Mathematicians, Data Analysts, Scientists, Accountants, Network Engineers and kids.
+ Ideal for first programming language
### Why is Python so special?
1. You can solve complex problems in less time with fewer lines of code. Example: let's extract first 3 characters of the text "Hello World" 
``` 
// C# code str.Substring(0, 3)

// JavaScript code str.substr(0, 3)

# Python code
str[0:3]
``` 
2. Python is multi-purpose language, used for: Data Analysis, AI / ML, Automation, Web Apps, Mobile Apps, Desktop Apps, Testing and Hacking. 
3. High-level language 
4. Cross-platform 
5. Huge Community 
6. Large Ecosystem

### Versions
Python 2 legacy Python
Python 3: future Python
### Python Interpreter
A program which executes Python code 
+ Examle of valid Python expresions: 
`>>> 2 + 2` 
`4` 
`>>> 2 > 1`
`True` 
`2 > 5` 
`False`

### First Python Program
```python 
print('Hello World 😹') # Hello World 😹 
print('*' * 10)         # **********
```
### Python Implementations
*Langugae: set of rules* 
*Implementation: a program* 
Example of implementations: 
+ CPython: Based on C 
+ Jython: Based on Java 
+ IronPython: Based on C#
+ PyPy: Based on subset of Python itself
---
# Primitive Types
---
### Variables
```python 
students_count = 1000               # integer 
rating = 4.99                       # float 
is_published = True                 # boolean 
is_verified = False                 # boolean 
course_name = 'Python Programming'  # string
```
### Strings
```python 
course = 'Python Programming' 
message = ''' Hi John,

This is Mosh from codewithmosh.com
''' 
print(len(course))  # 18 
print(course[0])    # P 
print(course[-1])   # g 
print(course[0:3])  # Pyt 
print(course[0:])   # Python Programming 
print(course[:3])   # Pyt 
print(course[:])    # Python Programming
```
### Escape Sequences
```python
# \"
# \'
# \\
# \n

course = 'Python \"Programming' # Python "Programming 
course = 'Python \'Programming' # Python 'Programming 
course = 'Python \Programming'  # Python \Programming 
course = 'Python \nProgramming' # Python 
                                # Programming 
```
### Formated Strings
```python
# Old way
first = 'Mosh' 
last = 'Hamedani' 
full = first + ' ' + last print(full) # Mosh Hamedani

# New way
first = 'Mosh' 
last = 'Hamedani' 
full = f"{first} {last}" 
print(full) # Mosh Hamedani

full = f"{len(first)} {2 + 2}" 
print(full) # 4 4 
```
### String Methods
```python 
course = 'Python Programming' 
print(course.upper())               # PYTHON PROGRAMMING 
print(course.lower())               # python programming 
print(course.title())               # Python Programming 
course = ' Python Programming ' 
print(course.strip())               # "Python programming" 
print(course.lstrip())              # "Python programming " 
print(course.lstrip())              # " Python programming" 
course = 'Python programming' 
print(course.find("P"))             # 0 
print(course.find("hon"))           # 2 
print(course.find("Programming"))   # -1 
print(course.replace('p', 'j'))     # Python jrogramming 
print('pro' in course)              # True
print('Programming' not in course)  # True
```
### Numbers
```python 
x = 1       # integer 
x = 1.1     # float 
x = 1 + 2j  # complex number (a + bi)

print(10 + 3)   # 13 
print(10 - 3)   # 7 
print(10 * 3)   # 30 
print(10 / 3)   # 3.3333333333333335 
print(10 // 3)  # 3 
print(10 % 3)   # 1 
print(10 ** 3)  # 1000

x = 10 
x = x + 3   # x += 3 
x += 3      # x = x + 3 
```
### Working with Numbers
```python 
import math

print(round(2.9))       # 3 
print(abs(-2.9))        # 2.9 
print(math.ceil(2.2))   # 3 
```
### Type Conversion
```python
# int()
# float()
# bool()
# str()

x = input('x: ') 
print(type(x))  # <class 'str'> 
y = x + 1       # TypeError: can only concatenate str (not "int") to str 
y = int(x) + 1  # Ok 
```
---
# Control Flow
---
### Comparison Operators
```python
# >
# <
# >=
# <=
# == 
# !=

print(10 > 3)           # True
print(10 >= 10)         # True
print(10 < 3)           # False
print(3 <= 10)          # True
print(10 == 10)         # True
print(10 == "10")       # False
print(10 != "10")       # True
print('bag' > "apple")  # True
print('bag' == 'BAG')   # False
print(ord('B'))         # 66
print(ord('b'))         # 98
```
### Conditional Statements
```python
"""
if condition1:
    pass
elif condition2:
    pass
else:
    pass
"""

temparature = 35
if temperature > 30:
    print("It's warm")      # It's warm
    print('Drink water')    # Drink water
print("Done")               # Done

temparature = 15
if temperature > 30:
    print("It's warm")
    print('Drink water')
print("Done")               # Done

temparature = 25
if temperature > 30:
    print("It's warm")
    print('Drink water')
elif temperature > 20:
    print("It's nice")      # It's nice
else:
    print("It's cold")
print("Done")               # Done
```
### Ternary Operator
```python
# variable = value1 if condition else value2

age = 22
if age >= 18:
    message = 'Eligible'
else:
    message = 'Not eligible'
print(message)  # Eligible

# Better way using ternary operator
message = 'Eligible' if age >= 18 else 'Not eligible'
print(message)  # Eligible
```
### Logical Operators
```python
# and
# or 
# not

high_income = True
good_credit = True

if high_income and good_credit:
    print('Eligible')   # Eligible
else:
    print('Not eligible')
    
high_income = True
good_credit = True
student = False

if (high_income or good_credit) and not student:
    print('Eligible')   # Eligible
else:
    print('Not eligible')
```
### Chaining Comparison Operators
```python
# age should be between 18 and 65
age = 22
if age >= 18 and age 65:
    print('Eligable')   # Eligible

# Cleaner way
if 18 <= age < 65:
    print('Eligale')    # Eligible
```
### For Loops
```python
for number in range(3):
    print('Attempt', number + 1)            # Attempt 1
                                            # Attempt 2
                                            # Attempt 3
                                    
for number in range(1, 8, 2):
    print('Attempt', number, '.' * number ) # Attempt 1 .
                                            # Attempt 3 ...
                                            # Attempt 5 .....
                                            # Attempt 7 .......
```