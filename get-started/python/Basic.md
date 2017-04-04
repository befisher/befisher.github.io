# Python 101

> Created by Fisher at 0:32 on 2017-03-11.

## Comments

```
# Single line comment.

“”””
This would be a multiline comment in Python that can take several lines.
“””
```


## Data Types

- `list(array)`         `[1, 2, 3]`
- `unit`          `(2, -5, 6)`
- `dictionary`    `{1: 'food', 2: 'taste', 3: 'good'}`
- `set`           `{'a', 'b', 'c'}`

## System Command Arguments

```py
# Run the test script.
python test.py Hello World

# ['test.py', 'Hello', 'World']
print(sys.argv)
```


## Functions

```
def func(arg1, arg2='default-value', arg3=10):
    global x
    # do something

def func(*arg0):
    # arg0 will be a unit
def func(**arg0):
    # arg0 will be a dictionary

def fun1(a, b, c):
    # do something
arg=(1, 2, 3)    # arg=[1, 2, 3]
fun1(*arg)
```


## Classes

```
class Obj(ParentClass):
    __private_params=1
    def __init__ (self):
        # init class
    @ staticmethod
    def func():
        # do something
    def __del__(self):
        # release resources
    def __add__:
    def __sub__:
    def __mul__:
    def __div__:
    def __le__:
    def __lt__:
    def __str__:
    def get_len:
obj = Obj()
obj._Obj__private_params  # access the private params for test
def newfunc():
    # do something
obj.newfunc = newfunc    # add new method to class
```
