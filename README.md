# Python-and-Pandas

#### #Create virtual environment
mkdir my_first_project
cd my_first_project/
python -m venv my_env_1

#### #Activate virtual environment
source my_env_1/bin/activate 

#### #Install packages to virtual environment
pip install pandas
pip install pandas==24.3.1

#### #List packages installed in environment
pip list

#### #Save installed packages to requirements file
pip freeze > requirements.txt

#### #Uninstal/Install packages according to requirement file 
pip uninstall -r requirements.txt
pip install -r requirements.txt

#### #Deactivate virtual environment 
deactivate

#### # import: 
Brings a module into the program's running memory so its contents can be accessed

#### # variable: 
A name that points to a piece of data

#### # assignment: 
Assigns a value to a variable

#### #expression: 
A piece of code that evaluates to a value

#### # exception: 
An error that stops execution of a program

import pandas as pd

//Create a variable pointing to a pandas Series

s = pd.Series([1, 2, 3]) 

//Assign a new variable pointing to the sum 

total = s.sum()  

//Update the variable with an expression

total += 10  

//Raise a pandas AttributeError exception

```python
try: 
    s.no_such_attribute() 
except AttributeError:
    print("Oops! That attribute doesn't exist")
```

#### # Function 
A named block of reusable code that can be executed multiple times. Defined using the def keyword.

#### # Parameters 
Variables that serve as inputs to a function. Specified within the parentheses in the function definition.

#### # Return statement 
Returns a value from the function. Used to define the output of a function.

#### # Default parameter value 
A value automatically assigned to a parameter if no argument is passed for that parameter in the function call. Defined using = in the function definition.

#### # Code block
The lines of code associated with and controlled by a programming statement. Indented under the statement.

#### # Function with two parameters 
def add_nums(num1, num2):
    sum = num1 + num2
    return sum
#### # Call function using parameters  
result = add_nums(5, 3)
print(result)
#### # Function with default parameter
def hello(name="John"):
    print("Hello " + name)
hello() # Uses default name 
hello("Jane") # Overrides default
#### # Function with code block
def print_lines():
    print("Line 1")
    print("Line 2")
    print("Line 3")
    
print_lines()

#### # Decorator
A function that takes another function as an argument, adds functionality, and returns the decorated function.

#### # Function decorator that times execution
```python
from time import time
def timer(func):
    # Nested wrapper function
    def wrapper():
        start = time()
        func()
        end = time()
        print(f"Duration: {end-start}")
    return wrapper
@timer
def sum_nums():
    result = 0
    for x in range(1000000):
        result += x
sum_nums()
```


Python has a number of operations that evaluate as one of the special values True or False. These include comparison operations, boolean operations, and object evaluations.

#### # Comparison Operations
Comparison can be made either by value or identity. Comparing by value are more generalized than comparison by value. The comparison operators that compare by value are:

== Equals

!= Not Equals

< Less Than

<= Less Than or Equal

> Greater Than

>= Greater Than or Equal

In most cases, two objects that are of different types will always evaluate as not equal. So the comparison 1 == 'b' will evaluate as False, and 1 != 'b' will evaluate as True. One notable exception to this is numeric types, such as integers and floating-point numbers. The comparison 1 == 1.0 will evaluate to True, and 1 != 1.0 will evaluate to False.

Run the code below to see the results of some equality comparisons. You can also try changing the values and running it again.

print( 1 == 'b' )
print( 1 != 2 )
print( 1 == 1.0 )
print( 1 == '1' )
print( 1 != 2 )
The order comparisons, those that test greater or less than values, will generally raise an error if the objects compared are of different types. A notable exception, again, is numeric types. The comparison 3.0 >= 2 will result in True. The order of objects depends on the type of objects being considered. For example text (type string), uses lexicographic order and numeric types use numeric order. Order comparison can be chained with multiple operators 1 < 2 <= 3 will result in True. Try running the examples below:
print( 1 < 33 )
print( 2 >= 2 )
print( 3.0 > 0 )
print( 'z' >= 'a' )
print( 1 <= 1.0 < 4 )
The comparison operators which compare by identity are is and is not. They are most commonly used to compare against the special object None.
print( 1 is None )
print( True is not None )


#### # Membership Operations
Some objects in Python can contain others. For example, the word "Henry" (of type string), contains the letter "r" (also a string). The in operator tests for this type of membership. The expression "r" in "Henry" will return True, and "b" in "Henry" will return False.

print('e' in 'Henry' )
print('a' not in 'Henry' )


#### # Boolean Operations
Boolean operations are based on boolean math, which you may have learned in a mathematics or philosophy course. The operators are and, or, and not. The first two take two operands, the last one, one operand. The and operator returns True if both of its operands evaluate as True and False if either evaluates to False. The or operator evaluates to True if either of its operands evaluates as True and False if they are both False. The not operator returns False if its operand evaluates to True and True otherwise. You can make more complex logical operations by nesting boolean operations in parenthesis. The expression (False and False) or (not False) evaluates to True, as not False is True.

print( True and False )
print( True and True )
print( False and True )
print( not True )
print( (False and False) or (not False) )


#### # Object Evaluations
All objects (everything) in Python evaluates as True or False. This means you can use them in the places where you would test for True or False, such as in Boolean operations. Generally, most Python objects evaluate as True. The exceptions are:

Numeric types that equal zero, such as 0, or 0.0.

The constants False and None.

Anything that has a length of zero. This includes the empty string, "".

print( 0 or 'a' )
print( 0 and 0.0 )
