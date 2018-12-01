## Python3 cheatsheet
##### Set up:
```python
$ brew install python3

$ mkdir project_env

# initialise environment
$ python3 -m venv ./project

# activate environment
$ source project_env/bin/activate

# your prompt will now read:
'(project_env)  ~/Development/projects'

# close environment
$ deactivate

# install packages:
# note pip3 is aliased to 'pip' in venv envs
$ pip install package_name
```
note `/projects` houses the environment, this is not where you should build your app. It just isolates the packages you install to your project.

envs to projects should have a 1-1 relationship.

##### Variables:
```python
use_snake_case = 'for variables'

# print to stdout
print(use_snake_case)
```
##### Most common primitives:
```python
# bool
this_is_true = True

# int / long
cats = 12
people = 7000000000

# float
pi = 3.14

# str
a_string = 'string'

# None - like nil (ruby) , or null (js)
nothing_here = None
```
##### Truthy / Falsy:
```python
# all values are truthy other than:
None
False
0
0.0
0j
Decimal(0)
Fraction(0, 1)

# empty:
[]    # list
{}    # dict
()    # tuple
''    # str
b''   # bytes
set()
range(0)

# objects for which
obj.__bool__() # returns False
obj.__len__() # returns 0

```

##### Booleans:
```python
True and False # -> False

True or False  # -> true

# negation
True and not False # -> True
```

##### Comparison operators:
```python
2 == 2  # -> True
2 != 2  # -> False
1 < 10  # -> True
1 > 10  # -> False
2 <= 2  # -> True
2 >= 2  # -> True
```

##### Control flow:
```python
# if-then-else
if True:
    print("true")
elif False:
    print("false")
else:
    print("not true or false")

# for loops - iterate over lists
for person in ["dave", "tom", "anne"]:
    print(person)

# use range to return an interable of numbers
for i in range(4):
    print(i)

# while loops
x = 0
while x < 5:
    print(x)
    x += 1  
```

##### User input from stdin:
```python
while 1: # infinite loop
    name = input("Name: ")
    if name == "":
        print("Ops! Retry")
    else:
        print("Hello", name)
        break  # this will break the loop
```

##### functions / methods
```python
# use explicit returns
def add(x, y):
    return x + y

# functions with out returns return None
def say(name):
    print(name)

a = say("ben")

print(a) # -> None
```
