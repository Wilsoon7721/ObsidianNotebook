### Basics

#### 1. Introduction

Python is a popular programming language as it is easy to learn and read. It can be used for many purposes such as web development, data analysis, artificial intelligence, and scripting. Python also supports Object-Oriented Programming (OOP).

Like all programming languages, Python has the same principles: 
   -  variables
   -  logical operators
   -  decision-making
   -  loops
   -  functions

#### 2. Syntax

An indent is an empty space at the beginning of a line. Usually, when writing paragraphs, you start a new paragraphs with 4 spaces before the start of the paragraph. Similarly, indentation in Python comes in multiples of 4 spaces.

Indentation is a significant part of the Python language. Indentation is used to define code blocks, such as enclosing if, for, and while loops instead of braces ('{ }').

An example of how indentation is performed is below:
```python
# Regular Code Flow
ready = True

if ready:
    # if statement code
    print("The code is ready!")
```


#### 3. Variables

Variables can be assigned in Python using the equal sign (`=`). Unlike some programming languages, Python does not require any specifying of a data type when assigning the variable as the data type of the variable is inferred from the assigned value.

From the above example, you may also see that variables can be assigned in the following format:
`variable_name = variable_value`

With the left-hand side being the name of the variable, and the right-hand side being the value.

Examples:
```python
message = "Hello world!"
age = 36   
amount_spent = 3510.75
```

#### 4. Data Types

While data types do not need to be specified when assigning variables in Python, the built-in data types should be understood so you know the different data they represent, as well as the available operations and expressions that each data type can be placed in.

##### Basic Types

**None**: Also known as NoneType, this represents the absence of a value, also known as `null`. 
**str**: Represents a string of characters, and are enclosed in either single quotes (`' '`) or double quotes (`" "`).
**bool**: Represents a Boolean value, either `True` or `False`.
**int**: Integers represent whole numbers, such as 13, -6, and 0.
**float**: Floating-point numbers represent numbers with decimal points, such as 16.41, -13.4 and 51.672. Integers can also be floats, and integers take on an additional `.0` behind whenever they are converted to floating-point values.

##### Other Types

**list**: A list in Python refers to an ordered, mutable collection of elements, with *mutable* meaning that the list can be modified when needed. An empty list can be created using square brackets as follows: `my_list = []`. Each element in a list is separated by a comma (`,`)

**tuple**: A tuple in Python is similar to a List, it's an ordered collection of elements, just that it is immutable, so once you create a tuple, it cannot be modified. An empty tuple can be created using regular brackets as follows: `my_tuple = ()`.

**dict**: Short form for dictionary, this is the Python equivalent of a map. A dictionary is an unordered, mutable collections of key-value pairs. This allows a value to be retrieved from a key. To pair a key to a value, a semicolon (`:`) is used. Similarly, dictionary entries are separated using commas (`,`). 
An example is as follows:
```python
capital_cities = {
	'Nepal': 'Kathmandu',
	'England': 'London',
	'Germany': 'Berlin',
	'Italy': 'Rome',
	'Vietnam': 'Hanoi'				  
}
```

After creating a dictionary like this, you may obtain the capital city of a country by using `capital_cities.get(key)`. Something like `capital_cities.get('Nepal')` will return `Kathmandu`.

Apart from using `.get(key)`, you may directly obtain the value using `capital_cities[key]`. An example would be like so:
```python
capital_england = capital_cities['England']
print(capital_england)
```

The code above would output `London`. As such, it shows that there are many ways of obtaining the same result, and it's up to you which one you prefer.

**set**: A set is an mutable, unordered collection of unique elements. Sets do not allow duplicate values and provide specific set operations such as union, intersection etc. More information on how to create a set is below.

**frozenset**: A frozenset is similar to set, except that it is immutable. Elements in a frozenset cannot be modified after being created. More information on how to create a frozenset is below.

**complex**: <u>You may not need to use this regularly as it is primarily meant for squaring an negative power.</u> A complex comes in the form of `a + bj`, where `a`  and `b` refer to real numbers while `j` is an imaginary value. More information on how to create a complex is below.

##### Sets, Lists, Tuples, and the Index Notation

Index Notation is used to identify the elements and their positions inside lists, sets, and tuples.

Simply put, elements in a collection start with `0` instead of `1`. For example,
```python
numbers = [0, 21, 516, 61, 134]

number = numbers[2]
print(number)
```

The above example will print `516`.  In index notation, the first value has an index of `0`. As such, the element at index `2` would refer to `516`. 

This logic applies to sets, lists, and tuples in Python, and is used in many popular programming languages. However, different languages may have their own ways of accessing the collection, with some using `.get(index)`, and others using regular brackets (`( )`) instead of square brackets (`[ ]`).

##### Creating and Manipulating Data Types

**None**: To set a variable as None, you can simply assign `None` as follows: `my_variable = None`.

**str**: Strings can be created using either the single or double quotes (`' '`, `" "`). However, in order to convert a variable into a String, a built-in function `str()` can be used to convert a value to string as follows: `number_string = str(58)`. The output is the same, but only the data type of the integer 58 and `number_string` are different.

**bool**: Booleans can be created simply by assigning a variable to either `True` or `False`. However, other data types do not explicitly need to be converted to Boolean before they can be used in a `True` or `False` context. However, to convert a value to a Boolean, a built-in function `bool()` can be used.

**int**: Like booleans, integers can be created by assigning a number value without decimals to a variable. However, to explicitly convert other data types such as strings into integers, a built-in function `int()` is available, with an example as follows: `number = int("101")`. This converts a String `"101"` into an integer of 101, before assigning it to `number`.

**float**: Floats can also be created by assigning a number value with decimals to a variable. Integers can also be represented as a float by adding a `.0` behind. To convert other data types such as strings, a built-in function `float()` can be used.

**list**: Lists can be created with the square brackets (`[ ]`). However, data types such as Strings can be converted to a list using the built-in `list()` function. Example: `my_list = list("hello")` would result in `my_list` being `['h', 'e', 'l', 'l', 'o']`.

**tuple**: Tuples can be created with regular brackets (`( )`). However, iterable data types such as lists can be passed to the built-in `tuple()` function to convert an existing list to a tuple.

**dict**: Dictionaries can be created with curly brackets (`{ }`). However, a list of key-value pairs can also be passed to the built-in `dict()` function to create a dictionary out of the existing data. Example: `my_dict = dict([('a', 1), ('b', 2)])` passes a list of two tuples into the dictionary, which is effectively a list of key-value pairs.

**set**: Sets can be created using the built-in `set()` function. An iterable such as a list or tuple should be passed to the `set()` function to create a set out of the existing data present.

**frozenset**: Frozen sets can be created using the built-in `frozenset()` function. Similar to `set()`, an iterable such as a list or tuple should be passed to the `frozenset()` function to create an immutable set out of the existing data present.

**complex**: Complexes can be created using the built-in `complex()` function. The `complex()` function accepts any value, and converts the resulting value to `(x + 0j)`, where `x` is the original value that you passed into the function. Example: `complex_value = complex(6)` would cause `complex_value` to have a value of `6 + 0j`. 


##### The Boolean Data Type

In Python, just about any data type can also be considered a Boolean. Different data types are compared for different things, before being evaluated to either `True` or `False`.

As such, while the `if` statement takes a condition and evaluates that, it is also able to evaluate other data types.

**int**, **float**, **complex** types are evaluated as `True` if they have any value other than zero, and `False` if the value is zero or if the value is None.

The **str** type are evaluated as `True` if the string is not empty, and `False` if the string is empty or if the value is None.

**list**, **tuple**, **dict**, **set**, **frozenset** types are evaluated as `True` if the list/tuple/dict/set is not empty, and `False` if the list/tuple/dict/set is empty.

Example:
```python
i = 56
message = "Hello!"
my_list = ['a', 'b', 'c', 'd', 'e']

if i:
    # Code Block
    print("'i' is not 0.")

if message:
	# Code Block
	print("'message' is not empty.")

if my_list:
    # Code Block
    print("'my_list' is not empty.")
```


#### 5. Functions

When you first start writing code, your first program may be to simply print "Hello World!". In order to accomplish this in Python, the `print()` function is called in your program, and the message is outputted as intended.

`print()` is one of the many functions built-in to the Python language, and a function refers to **a reusable piece of code that performs one or multiple tasks.** The piece of code is encapsulated into a named block, which can be called at any time whenever the same task needs to be performed multiple times.

In Python, functions can be defined with the `def` parameter before the function name. Similar to variables, functions do not have to specify a data type to indicate the return result.

Example Scenario:
```
Calculate the area of three different circles.
The 1st circle has a radius of 6, the 2nd circle has a radius of 8 and the last circle has a radius of 13.
```

The code would look like:
```python
pi = 3.14159
def calculate(radius):
    return pi * radius ** 2

circle1_area = calculate(6)
circle2_area = calculate(8)
circle3_area = calculate(13)
print("The area of circle 1 is", circle1_area)
print("The area of circle 2 is", circle2_area)
print("The area of circle 3 is", circle3_area)
```

From the code example, instead of performing the calculation 3 separate times with different radius values, the definition of `calculate()` allowed the program to be shortened, which overall allows the code to look cleaner.

##### 5.1: Function Parameters

As seen above, some functions take in **parameters**, and you are able to create your own functions that accept parameters too. In Python, if you run a function without inputting the required parameters, the IDE may throw a warning. However, you can choose to ignore the warning if you intended on running the function without giving the parameters.

Parameters are also similar to variables in Python such that they **do not have** any specific data type. As such, the user running your function can choose to put any parameter they want, and your code has to handle anything you don't want the function to process. However, **type hints** can be provided in your functions to drop a hint on what type you want the parameter to be. However, it **does not force** the user to give that specific data type.

Example:
```python
def add(a: float, b: float, c: float):
	if isinstance(a, float) and isinstance(b, float) and isinstance(c, float):
	    return a + b + c
	return "Invalid parameters given."

result = add("not a float", 10.5, 12.6)
print(result)
```

In the example shown, `a`, `b` and `c` are parameter names, and adding `: (type)` behind the parameter name created a type hint of `float`, hinting to the user and compiler that `a`, `b` and `c` should be floats.

Within the code itself, there's a built-in function known as `isinstance(value, type)` that accepts a value as the first parameter, and a type as the second. The purpose of the `isinstance(value, type)` function is to check if a value is an instance of a type. In this case, it checks if `a`, `b`, `c` are all instances of `float`, and using the `and` keyword, only allows the program to `return` the computation of all 3 when the condition is `True`.

In the case of the example shown, the result is `Invalid parameters given.` since the first parameter given is not a `float`, but a `string`.

#### 6. Decision Making

Like many other programming languages, Python provides decision making statements in the form of `if`, `elif`, and `else` statements.

Remember that once the first condition is met, the entire code block is exited and the other conditions will not be evaluated.

A full if-elif-else code block looks like the following:
```python
if condition:
    read_something()
elif second_condition:
    draw_something()
elif third_condition:
    send()
else:
    delete_everything()
    
print("The program will continue from here.")
```

As the if statement starts the code block, it is **compulsory**. The `elif` and `else` portions are not compulsory. If there is no `else` statement, the program directly skips to the code block below the entire `if` block.

From the code example above, the if the first condition is met, it performs the `read_something()` function and continues to the `print()` statement below. However, if the first condition is not met, it moves onto the first `elif` block, which checks for whether `second_condition` is met. If so, it runs `draw_something()` and moves on to the `print()` statement. However, if `second_condition` is not met, it moves on to check `third_condition`, and runs `send()` if the condition is met before exiting to the `print()` statement below. However, if none of the conditions are met, the code block in the `else` statement will run, which performs the `delete_everything()` function, before exiting to the print() statement.

Regardless of which condition is met, after the entire if-elif-else block finds its first met condition, the code within that specific condition block will be ran, and the program will skip the remaining checks and move on to the code below the entire `if-elif-else` block.

As such, when you are programming, it is important to order your conditions properly such that your intended result is reached.

#### 7. Operators

General operators:
   - `==` (equal to)
   - `!=` (not equal to)


##### 7.1: Numeric Operators

Numeric Operators refer to your regular operators that you may perform in Mathematics, such as:
   - `+` (add)
   - `-` (subtract)
   - `*` (multiply)
   - `**` (exponentiation)
   - `/` (divide)
   - `//` (floor divide)
   - `%` (modulo)

There are also the usual comparison operators:
   - `>` (greater than)
   - `<` (less than)
   - `>=` (greater than or equal to)
   - `<=` (less than or equal to)



For each of the numeric operators, there is a variation of it, where a `=` is added behind the operator, such as `+=`, `-=`, `*=`, `**=`, `/=`, `//=`, `%=`. These are called assignment operators, so something like "modulo assignment operator" would refer to the `%=` operator. An example of how the multiplication assignment operator is used is shown below:
```python
# Declare variable x
x = 14
print(x) # Prints '14'

# Multiply x by 2, and assign it back to x.
x *= 2
print(x) # Prints '28'
```

In the example, `x` is first declared as 14 and printed. Then, the `x *= 2` is performed and `x` is printed again. This time, `x` becomes 28. This is because `x *= 2` is the same thing as `x = x * 2`, which multiplies x by 2, but instead of assigning to another variable, the program assigns the new value back to the same value. As such:
```python
x = 15

x * 5

x *= 2
```

The computation `x * 5`  multiplies `x` by 5 but doesn't assign the new value to any variable, as such the result is not saved. However, `x *= 2` multiplies `x` by 2 and assigns the new value back to `x`, causing `x` to become 30. As such, these operators are known as **assignment operators**.

Exponentiation raises the value's power to that of the right side. Example: `b = 2 ** 4` will cause `b` to have a value of `2^4` which is 16.

Floor division is the same as regular division, just that instead of returning the full value with the decimals, it returns the **nearest whole number**.

Modulo returns the **remainder** of a division instead of the quotient.


##### 7.2: Logical Operators

Logical Operators refer to symbols or a word used to combine or manipulate boolean expressions.
The 3 most common logical operators are:
   - `AND` 
   - `OR` 
   - `NOT` 

Example:
```python
a = True 
b = False
if a and b:
    print("Both 'a' and 'b' are True!")

if a or b:
    print("Either 'a' or 'b' is True!")

if not a and not b:
	print("Both 'a' and 'b' are False!")
```

From the provided example, only the middle `print()` statement will pass, and the resulting code will print `Either 'a' or 'b' is True!`. The displayed example shows the usage of `AND`, `OR` and `NOT` to modify how the program evaluated each of the conditions.

While the first two are self-explanatory, the third one may require some explanation.

`not a` changes the check for the boolean `a`, so instead of checking whether `a` is True, the program instead checks if `a` is False. Similarly, `not b` causes the program to check whether `b` is False instead of `True`. The `and` keyword then joins both the conditions together, causing the code to check if both a and b is False before executing the code block. Of course, the code block didn't run because the initialized variables show that only `b` is False.


#### 8. Loops

Apart from `if` statements which asks the program to make decisions, loops allow the program to repeat a specific task repeatedly. This is achieved using the `for` loop and `while` loop.


##### 8.1: The For Loop

The syntax of a `for` loop is as follows:
```python
for something in iterable:
    # do this
```
Do take note that `something` and `iterable` are just variable names to display its purpose easier, and can be renamed anything you deem fit.

`iterable` usually refers to anything that can be repeated over and over again. Iterable data types usually refer to lists, sets and dictionaries, as these data types are most commonly used whenever there's a need to perform an action on all elements inside the object one by one.

In the above syntax, it translates to "for each item in `iterable`, assign the item to `something`, and perform the code inside the `for` block."

An example of the `for` loop is as follows:
```python
alphabets = ['abc', 'def', 'ghi', 'jkl', 'mno', 'pqr', 'stu', 'vwx', 'yz']
for value in alphabets:
	print(value)
```

This code will print the following:
```
abc
def
ghi
jkl
mno
pqr
stu
vwx
yz
```

From what you see here, each item inside the list was taken out, the item is then assigned to the `value` variable before `print(value)` is ran. This means that the `for` loop caused its code block to run 9 times, each with a different value from the list. The `for` loop retrieved each of the values in the order they were defined and printed them out one by one.

Another example of the `for` loop is as follows:
```python
numbers = [19, 519, 616, 123, 851, 167]
total = 0

for numb in numbers:
    total += numb

print(total)
```

This code defines a list of numbers and a variable `total` set to 0. The `for` loop then gets each number from the list and sets `numb` to the value of each number, before running `total += numb`, which adds the value into the total. This process is then repeated for all the numbers in the list. 

After finishing the loop, the program moves on to the code after the `for` loop, which prints the `total` variable out which is `2295`. 


##### 8.2: The While Loop

The syntax of a `while` loop is as follows:
```python
while condition:
    # What should the program do while the condition is NOT met.

# Continue
print("The condition was met.")
```

A `while` loop performs a piece of code continuously until a specific condition is met.

An example is below:
```python
i = 0

while i < 10:
    print(i)
    i += 1

print("The value of i has reached 10.")
```

In the above example, `i` is first initialized with a value of 0. Inside the `while` loop, the condition is set to `i < 10`, and the code inside will print the value of `i` before increasing `i` by 1. 

From the code, the program checks if `i` is less than 10. 
 - If yes, `i` is printed before being increased by 1. 
 - Then, `i` is checked again for whether its less than 10. 
 - If yes, the same process is repeated continuously until `i` is no longer less than 10. 
 - When that happens, the `print()` statement below is executed, stating that the value of `i` has reached 10.


#### 9. Flow Control

There are 3 keywords in Python that help to control the code flow. They are `return`, `break`, `continue`. 

The `return` statement is used only in functions to end the function's execution and return a result at the end of the function. However, it is **not compulsory** to `return` anything. When no `return` statement is provided, Python will automatically `return` the default value of `None`.

The `continue` and `break` statements are used only in loops such as the `while` and `for` loops.
The `break` statement stops all future iterations of the loop, and skips to the code below the loop, while the `continue` statement skips the current iteration of the loop, but does not stop future iterations.

Example:
```python
def add_five_to_value(number):
	return number + 5

numbers = [15, 18, 61, 71, 12, 16, 86, 92]
results = []
for i in numbers:
	if i == 61:
	    results.append(i) 
	    continue
	if i == 12:
		break
	result = add_five_to_value(i)
	results.append(result)

print(results)
```

The code demonstrates the use of both the `continue` and `break` statements.

Firstly, a function `add_five_to_value()` is defined which accepts a parameter called `number`. The function then returns a value of `number + 5`. Then, a list of 8 numbers is initialized and set to `numbers`. Another empty list is set to `results` as well. 

In the `for` loop, the program loops through each of the numbers in the original list, and does the following checks:
  1. If `i` is equal to 61, directly append `i` (61) to the results list, before executing `continue` which prevents the rest of the code in the loop from running. However, the `for` loop will not end there and continues to loop through the other numbers.
  
  2. If `i` is equal to 12, execute `break` which stops the rest of the code in the loop from running, and also stops the other numbers from being looped through. As such, the `for` loop ends there and the program skips to the code below the `for` loop, which prints the `results` list.

As such, the output of this program will be `[20, 23, 61, 76]`.


Another keyword that doesn't control the flow of the program, but is still useful is `pass`. 

The `pass` statement is simply a placeholder for future code, or to mark a loop or `if` statement purposely left empty. Nothing happens when the program executes it. However, since empty loops and statements are not allowed in Python, this statement is here to prevent those errors from occurring. 


#### 10. File Operations


##### The open() function


File operations can be performed using built-in functions such as `open()`.

The syntax of the `open()` function is `open(filename, mode)`.

`filename` refers to the name of the file you want to open. By default, if no file path is specified, Python searches for the file in its current directory (where your project and `.py` file may be).

`mode` should be a String value, and there are 7 valid modes, and 2 different types:
 1. `r` - read only
 3. `w` - write only
 4. `a` - append only
 5. `r+` - read and write. If the file doesn't exist, an exception is raised.
 6. `w+` - read and write. If the file doesn't exist, the file will be created.
 7. `a+` read and append. If the file doesn't exist, the file will be created.
 8. `x` - create the file and open as write. If the file already exists, an exception is raised.
Types:
 1. `b` - open file in binary
 2. `t` - open file in text (default)

Files are made up of a sequence of bytes, and each byte represents a unit of data within the file. When a file is opened in binary mode, it allows you to read and modify the file at the byte level. 

However, modifying files at byte level should be done with caution as randomly modifying files at byte level may cause the file to become corrupted. 

To specify the type, you may specify either `b` or `t` before the `+` sign, something like `rb` (read binary), `wb` (write binary) or `rb+` (read and write in binary).

##### Handling the file 

When files are opened, the handle to the file must also be closed when you are done reading or modifying the file.

```python
# Open `file.txt` in read mode.
f = open("file.txt", 'r')

# Read the data using the read() method and assign it to 'data'.
data = f.read()

# Close the file handle.
f.close()
```

It is important to close file handles after you have finished reading or modifying the files. Some reasons may include:
1. Resource Management - When files are opened, the system allocates memory and other resources to keep the file open. If the file isn't closed, the system will continue to allocate its resources to the file, resulting in resource leaks which could cause the system to crash due to high memory usage and other potential issues.

2. File Locks - When a file is opened by your program, other programs may not be able to access the file as the program places a lock on the file, informing other processes that your program is currently reading or modifying the file contents. This ensures that your program's file modifications can be saved properly without interruptions from other processes. However, if the file handle isn't closed, the lock remains on the file and other processes that require the file cannot access it, which could cause other processes to crash.

3. Data Integrity - When you write data to a file, the written data may remain in the memory, with the data only being written to the file right before the file handle is closed. This is used to improve efficiency by reducing the amount of times a write operation has to be done. As such, if the file handle is not closed, data may be partially saved or not saved at all, resulting in data loss. 

With that being said, there is code you can implement in Python that ensures that file handles are closed automatically when you are done with your code. An example is the `with` statement, with the syntax as such:
```python
with <expression> as <variable>:
    # Code Block
```

With the introduction of `with` and `as`,  performing file operations can be done as such:
```python
with open("diary.txt", 'r') as diary:
	data = diary.read()
	# Perform other file operations

print(data)
```

After the file is read inside the `with` block, the file handle is closed automatically without the need for `diary.close()`. This helps to keep the code clean while ensuring that resources are released when no longer needed.


#### 11. Exception Handling

Errors, also known as exceptions, occur in every programming language. Simply put, they are unexpected issues that are raised by the program when it's attempting to perform its task. Unexpected exceptions that are not caught cause the program to stop. However, if you know that the exception is going to occur, and want the program to continue running or want the program to print out the error, you may use the `try-except` block in Python to achieve this purpose. 

It is very beneficial to know that different scenarios may cause the same error, so you should not tie one specific error to one specific scenario.

There are many different errors you may experience, such as:
   1. ValueError - a reason why this may occur is if you are trying to convert a value using functions such as `int()`, `float()` or `str()`, and the value cannot be converted, it raises a ValueError.
   2. TypeError - a reason why this may occur could be if you are trying to concatenate a String and an Integer together.
   3. FileNotFoundError - As the error says, this error could most likely be raised if the file you are trying to `open()` cannot be found. Files will automatically be created if the `open()` mode is set to write or any other equivalent. However, if the file is opened in read mode and the file does not exist, a `FileNotFoundError` is raised instead.
   4. FileExistsError - As the error says, this error could most likely be raised by the `open()` mode set to `x`, also known as exclusive creation mode. In this mode, if the file doesn't exist, it is automatically created and the `open()` method is set to write. However, if the file already exists, a `FileExistsError` is raised instead.
   5. IndexError - IndexError could most likely be raised by attempting to access a list index that does not exist. Creating a variable like `my_list = [713, 1223, 6723]` and trying to run `number = my_list[5]` will raise this error as the index `5` does not exist in `my_list`.
   6. ZeroDivisionError - As the error says, this error is most likely raised by attempting to divide a value by zero.
   7. KeyError - A KeyError could most likely be caused by attempting to access a key in a dictionary which does not exist. Creating a dictionary like so: `bio = {"Name": "John", "Number": 12345678, "Country of Residence": "Singapore"}` and performing something like `print(bio['occupation'])` will raise the KeyError.

Handling exceptions can be done in many ways, with this being one of the most common ones:
```python
try:
    # Do your code that may or may not raise an error.
except ValueError:
    # A ValueError actually got raised, what should the code do.
```
In this above code, the `try-except` block does not have any direct access to the error itself. It just knows that the type of error that was thrown is a `ValueError`.

However, you can change that by including the `as` statement too.
```python
try:
    # Do your code that may or may not raise an error.
except ValueError as e:
    # A ValueError actually got raised, and the actual exception is `e`.
    print("Error occurred:", str(e))
```

In this modified code, the actual exception is assigned to the `e` variable using `except ValueError as e`. The error is then printed out by the `print()` statement, which converts `e` to a string using `str()`. This shows the error message in an easy-to-read format.

`try-except` blocks can also be nested and stacked.
An example would be:
```python
try:
    try:
        result = 95 / 0
    except ZeroDivisionError as e:
        # Handle ZeroDivisionError
        print("Error: You divided by zero.", e)
    except ValueError as e:
        # Handle ValueError
		print("Error: A value was wrongly parsed.", e)
except Exception as e:
    # Handle any other exception
    print("Error:", e)
```

If you are unsure of which exception to place in the `except` block, you may decide to use the same `except` block for all errors, which can be achieved in two different ways:

First method:
```python
try:
    # Code that may cause error
except:
    # Handle any error
```

In this first method, no error is specified, and as such it will default to using the same code for all exceptions encountered in the program. However, this also means that you may not be able to read the error message as there is no `e` variable being assigned.

Second method:
```python
try:
    # Code that may cause error
except Exception as e:
    # Handle any error as e
    print("Error:", e)
```

In this second method, the general `Exception` is specified, which refers to every single exception in Python. This is because for classes to be considered an Exception class, they must be a subclass of the `Exception` class. However, this time it is possible to except every exception as `e` and handle them separately.


With the introduction to handling exceptions done, there comes the `raise` keyword. The `raise` keyword is used to throw general and also custom exceptions from within your program. This means that you are able to create your own exceptions and raise them from within your own program, which can overall be used to signal an issue with your program.

An example of how the `raise` keyword is performed is as such:
```python
class PositiveValueError(Exception):
	pass

value = int(input("Give me a positive number: "))

try:
	if value < 0:
		raise PositiveValueError("Expected a positive number.")
	print("Thank you for the positive number.")
except PositiveValueError as e:
	print(e) # Prints 'Expected a positive number.'
```

In the following example, a custom Exception class called `PositiveValueError` is first declared. Then, a value is requested from the user. If the user inputs a value less than 0, the `PositiveValueError` is raised, before being caught by the `try-except` block inside the same code. The `PositiveValueError` variable called `e` is printed, which prints out the message that you input when you first raised the error. 


#### 12. External Libraries



#### End: Conclusion and other useful things.


Over here, you will find different built-in functions that help you to achieve different functionalities, such as asking for input or getting the maximum or minimum value from an iterable.