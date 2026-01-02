**Python Functions**





A function is a block of code which only runs when it is called.



A function can return data as a result.



A function helps avoiding code repetition.



Creating a Function

In Python, a function is defined using the def keyword, followed by a function name and parentheses:



Example

def my\_function():

&nbsp; print("Hello from a function")

This creates a function named my\_function that prints "Hello from a function" when called.



The code inside the function must be indented. Python uses indentation to define code blocks.



Calling a Function

To call a function, write its name followed by parentheses:



Example

def my\_function():

&nbsp; print("Hello from a function")



my\_function()

You can call the same function multiple times:



Example

def my\_function():

&nbsp; print("Hello from a function")



my\_function()

my\_function()

my\_function()

Function Names

Function names follow the same rules as variable names in Python:



A function name must start with a letter or underscore

A function name can only contain letters, numbers, and underscores

Function names are case-sensitive (myFunction and myfunction are different)

Example

Valid function names:



calculate\_sum()

\_private\_function()

myFunction2()

It's good practice to use descriptive names that explain what the function does.



Why Use Functions?

Imagine you need to convert temperatures from Fahrenheit to Celsius several times in your program. Without functions, you would have to write the same calculation code repeatedly:



Example

Without functions - repetitive code:



temp1 = 77

celsius1 = (temp1 - 32) \* 5 / 9

print(celsius1)



temp2 = 95

celsius2 = (temp2 - 32) \* 5 / 9

print(celsius2)



temp3 = 50

celsius3 = (temp3 - 32) \* 5 / 9

print(celsius3)

With functions, you write the code once and reuse it:



Example

With functions - reusable code:



def fahrenheit\_to\_celsius(fahrenheit):

&nbsp; return (fahrenheit - 32) \* 5 / 9



print(fahrenheit\_to\_celsius(77))

print(fahrenheit\_to\_celsius(95))

print(fahrenheit\_to\_celsius(50))

Return Values

Functions can send data back to the code that called them using the return statement.



When a function reaches a return statement, it stops executing and sends the result back:



Example

A function that returns a value:



def get\_greeting():

&nbsp; return "Hello from a function"



message = get\_greeting()

print(message)

You can use the returned value directly:



Example

Using the return value directly:



def get\_greeting():

&nbsp; return "Hello from a function"



print(get\_greeting())

If a function doesn't have a return statement, it returns None by default.



The pass Statement

Function definitions cannot be empty. If you need to create a function placeholder without any code, use the pass statement:



Example

def my\_function():

&nbsp; pass









**Python Function Arguments:**







Arguments

Information can be passed into functions as arguments.



Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.



The following example has a function with one argument (fname). When the function is called, we pass along a first name, which is used inside the function to print the full name:



Example

A function with one argument:



def my\_function(fname):

&nbsp; print(fname + " Refsnes")



my\_function("Emil")

my\_function("Tobias")

my\_function("Linus")

Parameters vs Arguments

The terms parameter and argument can be used for the same thing: information that are passed into a function.



From a function's perspective:



A parameter is the variable listed inside the parentheses in the function definition.



An argument is the actual value that is sent to the function when it is called.



Example

def my\_function(name): # name is a parameter

&nbsp; print("Hello", name)



my\_function("Emil") # "Emil" is an argument

Number of Arguments

By default, a function must be called with the correct number of arguments.



If your function expects 2 arguments, you must call it with exactly 2 arguments.



Example

This function expects 2 arguments, and gets 2 arguments::



def my\_function(fname, lname):

&nbsp; print(fname + " " + lname)



my\_function("Emil", "Refsnes")

If you try to call the function with the wrong number of arguments, you will get an error:



Example

This function expects 2 arguments, but gets only 1:



def my\_function(fname, lname):

&nbsp; print(fname + " " + lname)



my\_function("Emil")

Default Parameter Values

You can assign default values to parameters. If the function is called without an argument, it uses the default value:



Example

def my\_function(name = "friend"):

&nbsp; print("Hello", name)



my\_function("Emil")

my\_function("Tobias")

my\_function()

my\_function("Linus")

Example

Default value for country parameter:



def my\_function(country = "Norway"):

&nbsp; print("I am from", country)



my\_function("Sweden")

my\_function("India")

my\_function()

my\_function("Brazil")

Keyword Arguments

You can send arguments with the key = value syntax.



Example

def my\_function(animal, name):

&nbsp; print("I have a", animal)

&nbsp; print("My", animal + "'s name is", name)



my\_function(animal = "dog", name = "Buddy")

This way, with keyword arguments, the order of the arguments does not matter.



Example

def my\_function(animal, name):

&nbsp; print("I have a", animal)

&nbsp; print("My", animal + "'s name is", name)



my\_function(name = "Buddy", animal = "dog")

The phrase Keyword Arguments is often shortened to kwargs in Python documentation.



Positional Arguments

When you call a function with arguments without using keywords, they are called positional arguments.



Positional arguments must be in the correct order:



Example

def my\_function(animal, name):

&nbsp; print("I have a", animal)

&nbsp; print("My", animal + "'s name is", name)



my\_function("dog", "Buddy")

The order matters with positional arguments:



Example

Switching the order changes the result:



def my\_function(animal, name):

&nbsp; print("I have a", animal)

&nbsp; print("My", animal + "'s name is", name)



my\_function("Buddy", "dog")

Mixing Positional and Keyword Arguments

You can mix positional and keyword arguments in a function call.



However, positional arguments must come before keyword arguments:



Example

def my\_function(animal, name, age):

&nbsp; print("I have a", age, "year old", animal, "named", name)



my\_function("dog", name = "Buddy", age = 5)

Passing Different Data Types

You can send any data type as an argument to a function (string, number, list, dictionary, etc.).



The data type will be preserved inside the function:



Example

Sending a list as an argument:



def my\_function(fruits):

&nbsp; for fruit in fruits:

&nbsp;   print(fruit)



my\_fruits = \["apple", "banana", "cherry"]

my\_function(my\_fruits)

Example

Sending a dictionary as an argument:



def my\_function(person):

&nbsp; print("Name:", person\["name"])

&nbsp; print("Age:", person\["age"])



my\_person = {"name": "Emil", "age": 25}

my\_function(my\_person)

Return Values

Functions can return values using the return statement:



Example

def my\_function(x, y):

&nbsp; return x + y



result = my\_function(5, 3)

print(result)

Returning Different Data Types

Functions can return any data type, including lists, tuples, dictionaries, and more.



Example

A function that returns a list:



def my\_function():

&nbsp; return \["apple", "banana", "cherry"]



fruits = my\_function()

print(fruits\[0])

print(fruits\[1])

print(fruits\[2])

Example

A function that returns a tuple:



def my\_function():

&nbsp; return (10, 20)



x, y = my\_function()

print("x:", x)

print("y:", y)

Positional-Only Arguments

You can specify that a function can have ONLY positional arguments.



To specify positional-only arguments, add , / after the arguments:



Example

def my\_function(name, /):

&nbsp; print("Hello", name)



my\_function("Emil")

Without the , / you are actually allowed to use keyword arguments even if the function expects positional arguments:



Example

def my\_function(name):

&nbsp; print("Hello", name)



my\_function(name = "Emil")

With , /, you will get an error if you try to use keyword arguments:



Example

def my\_function(name, /):

&nbsp; print("Hello", name)



my\_function(name = "Emil")

Keyword-Only Arguments

To specify that a function can have only keyword arguments, add \*, before the arguments:



Example

def my\_function(\*, name):

&nbsp; print("Hello", name)



my\_function(name = "Emil")

Without \*,, you are allowed to use positional arguments even if the function expects keyword arguments:



Example

def my\_function(name):

&nbsp; print("Hello", name)



my\_function("Emil")

With \*,, you will get an error if you try to use positional arguments:



Example

def my\_function(\*, name):

&nbsp; print("Hello", name)



my\_function("Emil")

Combining Positional-Only and Keyword-Only

You can combine both argument types in the same function.



Arguments before / are positional-only, and arguments after \* are keyword-only:



Example

def my\_function(a, b, /, \*, c, d):

&nbsp; return a + b + c + d



result = my\_function(5, 10, c = 15, d = 20)

print(result)









**Python \*args and \*\*kwargs**









**\*args and \*\*kwargs**

**By default, a function must be called with the correct number of arguments.**



**However, sometimes you may not know how many arguments that will be passed into your function.**



**\*args and \*\*kwargs allow functions to accept a unknown number of arguments.**



**Arbitrary Arguments - \*args**

**If you do not know how many arguments will be passed into your function, add a \* before the parameter name.**



**This way, the function will receive a tuple of arguments and can access the items accordingly:**



**Example**

**Using \*args to accept any number of arguments:**



**def my\_function(\*kids):**

  **print("The youngest child is " + kids\[2])**



**my\_function("Emil", "Tobias", "Linus")**

**Arbitrary Arguments are often shortened to \*args in Python documentation.**



**What is \*args?**

**The \*args parameter allows a function to accept any number of positional arguments.**



**Inside the function, args becomes a tuple containing all the passed arguments:**



**Example**

**Accessing individual arguments from \*args:**



**def my\_function(\*args):**

  **print("Type:", type(args))**

  **print("First argument:", args\[0])**

  **print("Second argument:", args\[1])**

  **print("All arguments:", args)**



**my\_function("Emil", "Tobias", "Linus")**

**Using \*args with Regular Arguments**

**You can combine regular parameters with \*args.**



**Regular parameters must come before \*args:**



**Example**

**def my\_function(greeting, \*names):**

  **for name in names:**

    **print(greeting, name)**



**my\_function("Hello", "Emil", "Tobias", "Linus")**

**In this example, "Hello" is assigned to greeting, and the rest are collected in names.**



**Practical Example with \*args**

**\*args is useful when you want to create flexible functions:**



**Example**

**A function that calculates the sum of any number of values:**



**def my\_function(\*numbers):**

  **total = 0**

  **for num in numbers:**

    **total += num**

  **return total**



**print(my\_function(1, 2, 3))**

**print(my\_function(10, 20, 30, 40))**

**print(my\_function(5))**

**Example**

**Finding the maximum value:**



**def my\_function(\*numbers):**

  **if len(numbers) == 0:**

    **return None**

  **max\_num = numbers\[0]**

  **for num in numbers:**

    **if num > max\_num:**

      **max\_num = num**

  **return max\_num**



**print(my\_function(3, 7, 2, 9, 1))**

**Arbitrary Keyword Arguments - \*\*kwargs**

**If you do not know how many keyword arguments will be passed into your function, add two asterisks \*\* before the parameter name.**



**This way, the function will receive a dictionary of arguments and can access the items accordingly:**



**Example**

**Using \*\*kwargs to accept any number of keyword arguments:**



**def my\_function(\*\*kid):**

  **print("His last name is " + kid\["lname"])**



**my\_function(fname = "Tobias", lname = "Refsnes")**

**Arbitrary Keyword Arguments are often shortened to \*\*kwargs in Python documentation.**



**What is \*\*kwargs?**

**The \*\*kwargs parameter allows a function to accept any number of keyword arguments.**



**Inside the function, kwargs becomes a dictionary containing all the keyword arguments:**



**Example**

**Accessing values from \*\*kwargs:**



**def my\_function(\*\*myvar):**

  **print("Type:", type(myvar))**

  **print("Name:", myvar\["name"])**

  **print("Age:", myvar\["age"])**

  **print("All data:", myvar)**



**my\_function(name = "Tobias", age = 30, city = "Bergen")**

**Using \*\*kwargs with Regular Arguments**

**You can combine regular parameters with \*\*kwargs.**



**Regular parameters must come before \*\*kwargs:**



**Example**

**def my\_function(username, \*\*details):**

  **print("Username:", username)**

  **print("Additional details:")**

  **for key, value in details.items():**

    **print(" ", key + ":", value)**



**my\_function("emil123", age = 25, city = "Oslo", hobby = "coding")**

**Combining \*args and \*\*kwargs**

**You can use both \*args and \*\*kwargs in the same function.**



**The order must be:**



**regular parameters**

**\*args**

**\*\*kwargs**

**Example**

**def my\_function(title, \*args, \*\*kwargs):**

  **print("Title:", title)**

  **print("Positional arguments:", args)**

  **print("Keyword arguments:", kwargs)**



**my\_function("User Info", "Emil", "Tobias", age = 25, city = "Oslo")**

**Unpacking Arguments**

**The \* and \*\* operators can also be used when calling functions to unpack (expand) a list or dictionary into separate arguments.**



**Unpacking Lists with \***

**If you have values stored in a list, you can use \* to unpack them into individual arguments:**



**Example**

**Using \* to unpack a list into arguments:**



**def my\_function(a, b, c):**

  **return a + b + c**



**numbers = \[1, 2, 3]**

**result = my\_function(\*numbers) # Same as: my\_function(1, 2, 3)**

**print(result)**

**Unpacking Dictionaries with \*\***

**If you have keyword arguments stored in a dictionary, you can use \*\* to unpack them:**



**Example**

**Using \*\* to unpack a dictionary into keyword arguments:**



**def my\_function(fname, lname):**

  **print("Hello", fname, lname)**



**person = {"fname": "Emil", "lname": "Refsnes"}**

**my\_function(\*\*person) # Same as: my\_function(fname="Emil", lname="Refsnes")**







**Python Scope**





Scope

A variable is only available from inside the region it is created. This is called scope.



Local Scope

A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.



Example

A variable created inside a function is available inside that function:



def myfunc():

&nbsp; x = 300

&nbsp; print(x)



myfunc()

Function Inside Function

As explained in the example above, the variable x is not available outside the function, but it is available for any function inside the function:



Example

The local variable can be accessed from a function within the function:



def myfunc():

&nbsp; x = 300

&nbsp; def myinnerfunc():

&nbsp;   print(x)

&nbsp; myinnerfunc()



myfunc()

Global Scope

A variable created in the main body of the Python code is a global variable and belongs to the global scope.



Global variables are available from within any scope, global and local.



Example

A variable created outside of a function is global and can be used by anyone:



x = 300



def myfunc():

&nbsp; print(x)



myfunc()



print(x)

Naming Variables

If you operate with the same variable name inside and outside of a function, Python will treat them as two separate variables, one available in the global scope (outside the function) and one available in the local scope (inside the function):



Example

The function will print the local x, and then the code will print the global x:



x = 300



def myfunc():

&nbsp; x = 200

&nbsp; print(x)



myfunc()



print(x)

Global Keyword

If you need to create a global variable, but are stuck in the local scope, you can use the global keyword.



The global keyword makes the variable global.



Example

If you use the global keyword, the variable belongs to the global scope:



def myfunc():

&nbsp; global x

&nbsp; x = 300



myfunc()



print(x)

Also, use the global keyword if you want to make a change to a global variable inside a function.



Example

To change the value of a global variable inside a function, refer to the variable by using the global keyword:



x = 300



def myfunc():

&nbsp; global x

&nbsp; x = 200



myfunc()



print(x)

Nonlocal Keyword

The nonlocal keyword is used to work with variables inside nested functions.



The nonlocal keyword makes the variable belong to the outer function.



Example

If you use the nonlocal keyword, the variable will belong to the outer function:



def myfunc1():

&nbsp; x = "Jane"

&nbsp; def myfunc2():

&nbsp;   nonlocal x

&nbsp;   x = "hello"

&nbsp; myfunc2()

&nbsp; return x



print(myfunc1())

The LEGB Rule

Python follows the LEGB rule when looking up variable names, and searches for them in this order:



Local - Inside the current function

Enclosing - Inside enclosing functions (from inner to outer)

Global - At the top level of the module

Built-in - In Python's built-in namespace

Example

Understanding the LEGB rule:



x = "global"



def outer():

&nbsp; x = "enclosing"

&nbsp; def inner():

&nbsp;   x = "local"

&nbsp;   print("Inner:", x)

&nbsp; inner()

&nbsp; print("Outer:", x)



outer()

print("Global:", x)

