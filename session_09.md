# Object Oriented Programming (OOP)

# Class


```python
# a class is a structure which has provision to hold data and functions
class Person:
    def __init__(self,name,id):
        self.name = name
        self.age = id
    def sayHello(self):
        print("Hello ! My name is "+ self.name)
p1 =Person("Dan", 12)
p1.sayHello()
```

    Hello ! My name is Dan
    


```python
# class Dog:
#     def __init__(self,name,age):
#         self.name = name
#         self.age = age
    
```

#### A basic class definition in Python typically includes the class keyword followed by the class name and a colon.


```python
#My_pet = Dog("Piku",3)
```


```python
#print(My_pet.name)
```

    Piku
    


```python
#print(My_pet.name,My_pet.age)
```

    Piku 3
    


```python
#My_pet2 = Dog("Rockey",5)
```


```python
#print(My_pet2.name,My_pet2.age)
```

    Rockey 5
    


```python
class Dog:
    def __init__(self,name,age,sound):
        self.name = name
        self.age = age
        self.sound = sound
    def say(self): # if we want to make any changes define here
        print(self.sound*2)
```


```python
My_pet = Dog("piku",4,"woof")
```


```python
print(My_pet.sound)
```

    woof
    


```python
My_pet3 = Dog("rocky",4,"woof!!")
```


```python
(My_pet3.say())
```

    woof!!woof!!
    


```python
class Animal:
    def __init__(self,name,age,sound):
        self.name = name
        self.age = age
        self.sound = sound
    def say(self): # if we want to make any changes define here
        print(self.sound)
        
```

## Creating objects of a particular class


```python
class Dog(Animal):
     def __init__(self,name,age):
         super().__init__(name,age,"Wolf")
     def action(self):
         print("Moves tails")

```

### Inheritance


```python
class Cat(Animal):
     def __init__(self,name,age):
         super().__init__(name,age,"Wolf")
     def action(self):
         print("Moves ears")
        
```


```python
cat_1 = Cat("hai",12,)

```


```python
cat_1.action()
```

    Moves ears
    


```python
# from abc import ABC, abstractmethod
# class Dog(ABC): # Abstract calss
#     def __init__(self,name):
#         self.name = name
#     @abstractmethod
#     def sound(self): # aBSTRACT mETHOD
#         pass # to pass this function withot error
    
```


```python
# calculator 
class calculator:
    def __init__(self,num1,num2):
        self.num1 = num1
        self.num2 = num2
    def sum(self):
        print(f"\nthe sum is {self.num1 + self.num2}")

    def sub(self):
        print(f"the difference is {self.num1 - self.num2}")

    def multi(self):
        print(f"the product is {self.num1 * self.num2}")

    def div(self):
        print(f"the division result is {self.num1 / self.num2}")
        
        
```


```python
calculate = calculator(int(input("Give the first number")),int(input("Give the second number")))

calculate.sum()
calculate.sub()
calculate.multi()
calculate.div()
```

    Give the first number 4
    Give the second number 5
    

    
    the sum is 9
    the difference is -1
    the product is 20
    the division result is 0.8
    


```python
from os import listdir
downloads = listdir(r'C:\Users\aadar\Downloads')
for i in downloads:
    if '.pdf' in i:
        print(i)
```

    bew_bescheid_20250204103333.pdf
    C 11 Academic.pdf
    Day_2_Practise_Problems.pdf
    Eidesstattliche Versicherung.pdf
    Exmatrikulationsbescheinigung.pdf
    Resume.pdf
    RWTH_Info_Studienaufnahme.pdf
    Screenshot 2025-02-08 095630.pdf
    Transcript.pdf
    


```python
for i in downloads:
    if ".mkv" in i:
        continue
    else:
        print(i, end = "\n")
```

    Add on 2.ipynb
    bew_bescheid_20250204103333.pdf
    C 11 Academic.pdf
    Class 2 Functions.md
    Dard - E - Disco ( DJ VK EXTENDED MIX ).mp3
    Day_2_Practise_Problems.pdf
    desktop.ini
    DiscordSetup.exe
    Eidesstattliche Versicherung.pdf
    Exmatrikulationsbescheinigung.pdf
    Git-2.48.1-64-bit.exe
    IELTS
    IMG-20250208-WA0000.jpg
    Programming_Foundationals
    python-3.13.2-amd64.exe
    Resume.pdf
    RWTH_Info_Studienaufnahme.pdf
    Screenshot 2025-02-08 095630.pdf
    Telegram Desktop
    Transcript.pdf
    VSCodeUserSetup-x64-1.97.2.exe
    Wondershare Filmora 14.3.2.11147 (x64) Multilingual [FileCR].zip
    


```python
from os import listdir
from os import path
from os.path import getsize


file_path = path.join('C:','Users','aadar','Downloads')
file_names = listdir(file_path)
for i in file_names:
    if ".mkv" in i:
        continue
    else:
        print(i, end = "\n")
```

    Add on 2.ipynb
    bew_bescheid_20250204103333.pdf
    C 11 Academic.pdf
    Class 2 Functions.md
    Dard - E - Disco ( DJ VK EXTENDED MIX ).mp3
    Day_2_Practise_Problems.pdf
    desktop.ini
    DiscordSetup.exe
    Eidesstattliche Versicherung.pdf
    Exmatrikulationsbescheinigung.pdf
    Git-2.48.1-64-bit.exe
    IELTS
    IMG-20250208-WA0000.jpg
    Programming_Foundationals
    python-3.13.2-amd64.exe
    Resume.pdf
    RWTH_Info_Studienaufnahme.pdf
    Screenshot 2025-02-08 095630.pdf
    Telegram Desktop
    Transcript.pdf
    VSCodeUserSetup-x64-1.97.2.exe
    Wondershare Filmora 14.3.2.11147 (x64) Multilingual [FileCR].zip
    


```python
for file_name in file_names:
    file_size = getsize(path.join('C:','Users','aadar','Downloads', file_name))
    print(file_name,"contains", file_size,"Kbs")
```

    Add on 2.ipynb contains 5609 Kbs
    bew_bescheid_20250204103333.pdf contains 215077 Kbs
    C 11 Academic.pdf contains 82722450 Kbs
    Class 2 Functions.md contains 5809 Kbs
    Dard - E - Disco ( DJ VK EXTENDED MIX ).mp3 contains 11062750 Kbs
    Day_2_Practise_Problems.pdf contains 163088 Kbs
    desktop.ini contains 282 Kbs
    DiscordSetup.exe contains 114019704 Kbs
    Eidesstattliche Versicherung.pdf contains 1049300 Kbs
    Exmatrikulationsbescheinigung.pdf contains 586103 Kbs
    Git-2.48.1-64-bit.exe contains 69544752 Kbs
    IELTS contains 12288 Kbs
    IMG-20250208-WA0000.jpg contains 58806 Kbs
    Programming_Foundationals contains 4096 Kbs
    python-3.13.2-amd64.exe contains 28604208 Kbs
    Resume.pdf contains 80947 Kbs
    RWTH_Info_Studienaufnahme.pdf contains 804555 Kbs
    Screenshot 2025-02-08 095630.pdf contains 315564 Kbs
    Telegram Desktop contains 0 Kbs
    Transcript.pdf contains 2905678 Kbs
    VSCodeUserSetup-x64-1.97.2.exe contains 105639336 Kbs
    Wondershare Filmora 14.3.2.11147 (x64) Multilingual [FileCR].zip contains 875600230 Kbs
    


```python
dict_file = {}
for name in file_names:
    file_size = getsize(path.join('C:','Users','aadar','Downloads', name))
    dict_file [file_size] = name

print(f"The file name {dict_file[max(dict_file.keys())]} has maximum size of {max(dict_file.keys())} kbs")
    
```

    The file name Wondershare Filmora 14.3.2.11147 (x64) Multilingual [FileCR].zip has maximum size of 875600230 kbs
    

# Python Practice Problems

1. Data Types and Operators
- Write a program to add two integers.
- Write a program to subtract two floats.
- Write a program to multiply two numbers.
- Write a program to divide two numbers and handle division by zero.
- Write a program to find the remainder of two numbers using the modulus operator.
- Write a program to swap two variables without using a third variable.
- Write a program to check if a number is even or odd.
- Write a program to find the square of a number.
- Write a program to find the cube of a number.
- Write a program to convert Celsius to Fahrenheit.

2. String Handling
- Write a program to concatenate two strings.
- Write a program to find the length of a string.
- Write a program to reverse a string.
- Write a program to check if a string is a palindrome.
- Write a program to count the number of vowels in a string.
- Write a program to convert a string to uppercase.
- Write a program to convert a string to lowercase.
- Write a program to replace a substring in a string.
- Write a program to check if a string starts with a specific prefix.
- Write a program to check if a string ends with a specific suffix.

3. Conditional Statements
- Write a program to find the largest of three numbers.
- Write a program to check if a number is positive, negative, or zero.
- Write a program to check if a year is a leap year.
- Write a program to check if a number is divisible by both 3 and 5.
- Write a program to check if a character is a vowel or consonant.
- Write a program to check if a number is within a given range.
- Write a program to compare two strings and print the larger one.
- Write a program to calculate the grade based on a student's score.
- Write a program to check if a number is a prime number.

4. Loops
- Write a program to print numbers from 1 to 10 using a for loop.
- Write a program to print numbers from 10 to 1 using a while loop.
- Write a program to print the multiplication table of a number.
- Write a program to find the sum of all numbers from 1 to 100.
- Write a program to find the factorial of a number.
- Write a program to print all even numbers between 1 and 50.
- Write a program to print the Fibonacci series up to n terms.
- Write a program to check if a number is an Armstrong number.
- Write a program to print the following pattern:
*
**
***
****
*****

- Write a program to find the sum of digits of a number.

5. Functions
- Write a function to add two numbers.
- Write a function to find the maximum of two numbers.
- Write a function to check if a number is prime.
- Write a function to reverse a string.
- Write a function to calculate the factorial of a number.
- Write a function to check if a string is a palindrome.
- Write a function to find the area of a circle.
- Write a function to find the GCD of two numbers.
- Write a function to find the LCM of two numbers.
- Write a function to print the first n terms of the Fibonacci series.

6. Lists
- Write a program to find the sum of all elements in a list.
- Write a program to find the largest element in a list.
- Write a program to find the smallest element in a list.
- Write a program to reverse a list.
- Write a program to count the occurrences of an element in a list.
- Write a program to remove duplicates from a list.
- Write a program to check if a list is sorted.
- Write a program to merge two lists.
- Write a program to find the second largest element in a list.
- Write a program to sort a list in ascending order.

7. Tuples
- Write a program to create a tuple and print its elements.
- Write a program to find the length of a tuple.
- Write a program to concatenate two tuples.
- Write a program to check if an element exists in a tuple.
- Write a program to find the index of an element in a tuple.
- Write a program to count the occurrences of an element in a tuple.
- Write a program to convert a tuple to a list.
- Write a program to reverse a tuple.
- Write a program to find the maximum element in a tuple.
- Write a program to find the minimum element in a tuple.

8. Dictionaries
- Write a program to create a dictionary and print its keys and values.
- Write a program to add a new key-value pair to a dictionary.
- Write a program to remove a key from a dictionary.
- Write a program to check if a key exists in a dictionary.
- Write a program to find the length of a dictionary.
- Write a program to merge two dictionaries.
- Write a program to find the sum of all values in a dictionary.
- Write a program to sort a dictionary by its keys.
- Write a program to sort a dictionary by its values.
- Write a program to find the key with the maximum value in a dictionary.

9. Sets
- Write a program to create a set and add elements to it.
- Write a program to remove an element from a set.
- Write a program to find the union of two sets.
- Write a program to find the intersection of two sets.
- Write a program to find the difference between two sets.
- Write a program to check if a set is a subset of another set.
- Write a program to check if two sets are disjoint.
- Write a program to find the length of a set.
- Write a program to clear all elements from a set.
- Write a program to convert a list to a set.

10. Basics of OOPs
- Write a class to represent a Rectangle with methods to calculate area and perimeter.
- Write a class to represent a Circle with methods to calculate area and circumference.
- Write a class to represent a Student with attributes like name, roll number, and marks.
- Write a class to represent a BankAccount with methods to deposit and withdraw money.
- Write a class to represent a Car with attributes like make, model, and year.
- Write a class to represent a Book with attributes like title, author, and price.
- Write a class to represent a Person with attributes like name and age, and a method to display details.
- Write a class to represent a Bank with methods to add accounts and display total balance.
- Write a class to represent a Shape with a method to calculate area, and create subclasses for Square and Circle.


```python

```
