<!-- PROJECT LOGO -->
<br />
<p align="center">
    <img src="../inputs/icons/speedometer.svg" alt="Logo" width="15% id="logo">
    <p  align="center" style="font-size:0.75em;">Icon made by <a href="https://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></p>
    <h1 align="center">Tips to speed up python codes</h1>
    <h2 align="center">Python Workshop - Leeds Institute for Data Analytics (LIDA)</h2>
</p>

## Disclaimer

> This repository is under construction. 
> The workshop will be held at October 2021.

## General solution

> To speed up any Python code four steps can be followed:

1. Before moving on to more advanced techniques, it is recommended to review the code, following a series of good practices. Some tips from these best practices (which lead to better code performance) are listed in the [General tips](#general-tips) session.
2. Once you have ensured that your code is *well written*, it is recommended to profile your code (see [CPU profiling](#cpu-profiling) and [Memory profiling](#memory-profiling) sessions).
3. It is possible to translate the Python function to an optimized code (see [Native-speed code](#native-speed-code) session).
4. Finally, it is possible to separate the running process in several processes to be run in parallel (see [Multiprocessing](#multiprocessing)).

---

## General tips

Before moving on to more advanced techniques, it is necessary to ensure that the code is written in the best possible way. Below, some practices considered ideal will be presented.

### Python version

> Every release is more optimized.

The latest version should have the best performance, so make sure you always use the latest version. At least choose Python 3 over Python 2.

### Data structure

> Using the most appropriate data structure is critical to speed up the code.

Python has some built-in data structures (namely: list, tuple, set, and dictionary). It is also possible to use additional data structures by importing modules (like [NumPy array](https://numpy.org/doc/stable/reference/generated/numpy.array.html) and [pandas DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)).

One of the most common mistakes is using the **list** structure for all cases. For example, if your list has elements of a single type (like real numbers), you might consider using a NumPy array to optimise the code.

### Assign variables

> Avoid assign variables inside loops.

Variables assigned within loops are recreated whenever the loop is iterated.

> Multiple assignments

If there is more than one variable to assign, you can perform a multiple assignment. The code:

```python
x, y, z = 1, 2, 3
```

is more efficient than

```python
x = 1
y = 2
z = 3
```

### Library function and dot operation

> Library functions are designed to be as efficient as possible.

Instead of writing your own functions, whenever possible use functions from existing libraries. Also, when using a library function, avoid using the dot operation. The following code:

```python
from math import sqrt

x = sqrt(4)
```

is more efficient than the code with dot operation:

```python
import math

x = math.sqrt(4)
```

that is more efficient than the code with a homemade function:

```python
x = 4 ** 0.5
```

### List comprehension

> List comprehension is a very concise syntax to create a new list

Create lists using *list comprehension* whenever possible. List comprehension can be used over:

- loops
- lambda function
- map()
- filter()
- reduce()

For example, to create a list of even numbers, you can change the following code:

```python
x = []
for i in range(100):
    if i%2 == 0:
      x.append(i)
```

for a list comprehension:

```python
x = [i for i in range(100) if i%2 == 0]
```

### If-else ladder

> Put high probability if-statements first!

Putting low probability if-statements early will make your code perform more operations than necessary.

---
