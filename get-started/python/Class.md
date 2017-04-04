# Class in Python

> Created by Fisher at 19:51 on 2017-03-11.

```py
class Test(ParentClass):
	# Static variable.
	sStaticVariable = 11;
	# Private variable.
    __private_params=1
    # Initialize class
    def __init__ (self):
		# Normal variable.
		self.name = 'Test Object'
		self.data = 'Test Object'
	def hello(self):
		print(self.name);
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

print(Test.sStaticVariable)

obj = Test()
obj._Obj__private_params  # access the private params for test
def newfunc():
    # do something
obj.newfunc = newfunc    # add new method to class
```
