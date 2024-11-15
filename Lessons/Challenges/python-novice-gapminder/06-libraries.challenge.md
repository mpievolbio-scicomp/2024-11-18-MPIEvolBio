
## Exploring the Math Module

1. What function from the `math` module can you use to calculate a square root
  *without* using `sqrt`?
2. Since the library contains this function, why does `sqrt` exist?


## Locating the Right Module

You want to select a random character from a string:

```python
bases = 'ACTTGCTTGAC'
```

1. Which [standard library][stdlib] module could help you?
2. Which function would you select from that module? Are there alternatives?
3. Try to write a program that uses the function.


## Jigsaw Puzzle (Parson's Problem) Programming Example

Rearrange the following statements so that a random
DNA base is printed and its index in the string.
Not all statements may be needed.  Feel free to use/add
intermediate variables.

```python
bases="ACTTGCTTGAC"
import math
import random
___ = random.randrange(n_bases)
___ = len(bases)
print("random base ", bases[___], "base index", ___)
```


## When Is Help Available?

When a colleague of yours types `help(math)`,
Python reports an error:

```error
NameError: name 'math' is not defined
```

What has your colleague forgotten to do?


## Importing With Aliases

1. Fill in the blanks so that the program below prints `90.0`.
2. Rewrite the program so that it uses `import` *without* `as`.
3. Which form do you find easier to read?

```python
import math as m
angle = ____.degrees(____.pi / 2)
print(____)
```


## There Are Many Ways To Import Libraries!

Match the following print statements with the appropriate library calls.

Print commands:

1. `print("sin(pi/2) =", sin(pi/2))`
2. `print("sin(pi/2) =", m.sin(m.pi/2))`
3. `print("sin(pi/2) =", math.sin(math.pi/2))`

Library calls:

1. `from math import sin, pi`
2. `import math`
3. `import math as m`
4. `from math import *`


## Importing Specific Items

1. Fill in the blanks so that the program below prints `90.0`.
2. Do you find this version easier to read than preceding ones?
3. Why *wouldn't* programmers always use this form of `import`?

```python
____ math import ____, ____
angle = degrees(pi / 2)
print(angle)
```


## Reading Error Messages

1. Read the code below and try to identify what the errors are without running it.
2. Run the code, and read the error message. What type of error is it?

```python
from math import log
log(0)
```

