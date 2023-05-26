
#### 1. General

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


**set**: A set is an mutable, unordered collection of unique elements. Sets do not allow duplicate values and provide specific set operations such as union, intersection etc. More information on how to create a set is below.

**frozenset**: A frozenset is similar to set, except that it is immutable. Elements in a frozenset cannot be modified after being created. More information on how to create a frozenset is below.

**complex**: <u>You may not need to use this regularly as it is primarily meant for squaring an negative power.</u> A complex comes in the form of `a + bj`, where `a`  and `b` refer to real numbers while `j` is an imaginary value. More information on how to create a complex is below.


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

