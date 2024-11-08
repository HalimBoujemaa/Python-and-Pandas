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