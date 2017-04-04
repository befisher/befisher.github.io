# List(Array) in Python

> Created by Fisher at 19:24 on 2017-03-11.

```py
# Init a list
m = [0,1,2,3,4,5,6,7,8,9,10]

# Slicing the list
mList = m[2:6]
mList = m[2:]
mList = m[:6]
m[0:2] = [12, 32]

# Accessing the elements
for e in m:
	print e

for i in range(len(m)):
	print m[i]

# Pop, Push, Shift, and Unshift
m.pop(100)
m.append()
m = [100] + m
m = m[1:]
```
