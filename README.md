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