# CONDITIONALS
 Conditionals let your program make decisions.
 if condition:
    # do something
elif another_condition:
    # do something else
else:
    # do this if none are true
# COMMON MISTAKES 
forgetting colon : at end
wrong indentation
using = instead of ==

# BOOLEAN EXPRESSIONS
Booleans are the simpliest values in programming: True or False. They're like yes/no questions your code asks.
True
False 
x == y # equal 
x != y # not equal 
x > y # greater than
x < y # less than 
x >= y # greater or equal 
x <= y # less or equal
and # both true
or # at least one true 
not # reverses boolean

# FUNCTIONS(def)

Functions are reusable recipes. Write code once , use i many times .

def function_name(parameter1, parameter2):
    """explaining what it does"""
    # body
    retun result

# main() PATTERN
the main() fuction is a convention , it's whre your program starts. the if__name__ == "__main__" part ensures code only runs when you run this file directly

def main():
    name = input("enter name")
    greet(name)
def greet(name):
    print(f"hello, {name}")

if __name__ == "__main__":
    main()

# DICTIONARIES
 Dictionaries store data in key-value pair.
 like a real dictionary you look up a word (key) and get its definition (value). or like labels on boxes

student = {
    "name": "maroua",
    "age": 20,
    "courses": ["CS", "Math"]
}

# Access
print(student["name"])
print(student.get("age"))  # Safer

# Modify
student["age"] = 21
student["city"] = "Nanchang"  # Add new

# Delete
del student["city"]
popped = student.pop("age")

# Methods
student.keys()      # dict_keys(['name', 'courses'])
student.values()    # dict_values(['maroua', ['CS', 'Math']])
student.items()     # dict_items([('name', 'maroua'), ('courses', ['CS', 'Math'])])
student.update({"grade": "A", "year": 2})

# Loop
for key, value in student.items():
    print(f"{key}: {value}")

# Lists
Lists store multiple items in order. You can add, remove, and access items by position.
# Create
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", True, 3.14]

# Access
first = fruits[0]      # apple
last = fruits[-1]       # orange

# Modify
fruits[1] = "grape"
fruits.append("mango")   # Add to end
fruits.insert(1, "kiwi") # Add at position
fruits.remove("apple")   # Remove by value
popped = fruits.pop()    # Remove and return last

# Methods
fruits.sort()
fruits.reverse()
len(fruits)
"apple" in fruits  # True/False

# Slicing
fruits[1:3]    # index 1 to 2
fruits[:2]     # start to index 1
fruits[2:]     # index 2 to end
fruits[-2:]    # last two

# For Loops
For loops let you repeat actions for each item in a collection. Like going through a list and doing something with every item.
# Loop through list
for fruit in fruits:
    print(fruit)

# Loop with index
for i in range(len(fruits)):
    print(i, fruits[i])

# Loop with enumerate
for i, fruit in enumerate(fruits):
    print(i, fruit)

# Loop through dictionary
for key in student:
    print(key)

for value in student.values():
    print(value)

for key, value in student.items():
    print(key, value)

# range() function
range(5)           # 0,1,2,3,4
range(1, 5)        # 1,2,3,4
range(1, 10, 2)    # 1,3,5,7,9


# String Slicing
Strings are sequences of characters. Slicing lets you extract parts - like cutting a piece from a rope.
text = "Hello, World!"

# Basic slicing [start:end:step]
text[0:5]     # "Hello"
text[7:12]    # "World"
text[:5]      # "Hello" (start from beginning)
text[7:]      # "World!" (go to end)
text[-6:-1]   # "World"
text[::2]     # "Hlo ol!" (every 2nd character)
text[::-1]    # "!dlroW ,olleH" (reverse)

# Common operations
text.upper()
text.lower()
text.split(", ")
text.replace("Hello", "Hi")
text.strip()  # remove whitespace
# Triple Quotes
Triple quotes let you write strings that span multiple lines. Like writing a paragraph instead of a single sentence.
# Multi-line string
message = """This is a
multi-line
string"""

# Docstrings
def my_function():
    """This is a docstring.
    It explains what the function does.
    Can be multiple lines."""
    pass

# Preserve formatting
poem = '''
Roses are red,
Violets are blue,
Python is awesome,
And so are you.
'''
# While Loops
While loops repeat as long as a condition is true. 
# Basic while
count = 0
while count < 5:
    print(count)
    count += 1

# User input loop
user_input = ""
while user_input != "quit":
    user_input = input("Enter something (or 'quit'): ")
    print(f"You entered: {user_input}")

# Infinite loop with break
while True:
    command = input("> ")
    if command == "exit":
        break
    if command == "":
        continue  # skip to next iteration
    print(f"Processing: {command}")

# Flag variable
running = True
while running:
    # do something
    if some_condition:
        running = False
# None
None represents nothing, emptiness, "no value yet." Like an empty box waiting to be filled.
# Represents "nothing" or "no value"
result = None
print(result)  # None

# Common use: variable placeholder
data = None  # will be set later

# Function returns None if no return
def say_hello():
    print("Hello")

result = say_hello()  # prints Hello
print(result)  # None

# Checking for None
if result is None:
    print("No value returned")

# None is falsy, but use 'is' to check
if not result:  # works but not best
    pass

if result is None:  # correct way
    pass

# sep (separator)
sep controls what goes between items when printing. Default is space, but you can change it to anything.
# Used in print() to separate multiple arguments
print("Hello", "World")  # Hello World (default sep=" ")
print("Hello", "World", sep="-")  # Hello-World
print("2024", "12", "25", sep="/")  # 2024/12/25
print("apple", "banana", "orange", sep=", ")  # apple, banana, orange

# Can use any string
print("A", "B", "C", sep="")    # ABC
print("X", "Y", sep="\n")        # X (newline) Y

# end
end controls what comes after printing. Default is newline, but you can change it to keep printing on same line.
# Used in print() to control what comes at the end
print("Hello")  # default end="\n" (newline)
print("World")
# Output:
# Hello
# World

# Remove newline
print("Hello", end="")
print("World")  # HelloWorld

# Add custom ending
print("Loading", end="...")
print("Done")  # Loading...Done

# Multiple prints on same line
for i in range(5):
    print(i, end=" ")  # 0 1 2 3 4 

# Progress indicator
import time
for i in range(10):
    print("█", end="", flush=True)
    time.sleep(0.2)
# Prints loading bar on same line

# len()
len() tells you how many items are in something. How many characters in a string, items in a list, keys in a dictionary.
# Returns length (number of items)
# Strings
text = "Python"
print(len(text))  # 6

# Lists
fruits = ["apple", "banana", "orange"]
print(len(fruits))  # 3

# Dictionaries
student = {"name": "Alex", "age": 20}
print(len(student))  # 2

# Tuples
coordinates = (10, 20, 30)
print(len(coordinates))  # 3

# Useful in loops
for i in range(len(fruits)):
    print(fruits[i])

# Check if empty
if len(my_list) == 0:
    print("List is empty")

# Alternative (Pythonic)
if not my_list:  # empty list is falsy
    print("List is empty")

# range()
Introduction:
range() generates sequences of numbers. Like a number line you can walk along.
# Generates sequence of numbers

# range(stop)
for i in range(5):
    print(i)  # 0 1 2 3 4

# range(start, stop)
for i in range(2, 6):
    print(i)  # 2 3 4 5

# range(start, stop, step)
for i in range(1, 10, 2):
    print(i)  # 1 3 5 7 9

# Negative step
for i in range(10, 0, -2):
    print(i)  # 10 8 6 4 2

# Convert to list
numbers = list(range(5))     # [0, 1, 2, 3, 4]
evens = list(range(0, 10, 2)) # [0, 2, 4, 6, 8]

# Common patterns
# Loop with index
fruits = ["apple", "banana", "orange"]
for i in range(len(fruits)):
    print(f"{i}: {fruits[i]}")

# Loop backwards
for i in range(len(fruits)-1, -1, -1):
    print(fruits[i])