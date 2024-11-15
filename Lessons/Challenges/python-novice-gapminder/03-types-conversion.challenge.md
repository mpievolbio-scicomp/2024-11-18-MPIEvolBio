
## Fractions

What type of value is 3.4?
How can you find out?


## Automatic Type Conversion

What type of value is 3.25 + 4?


## Choose a Type

What type of value (integer, floating point number, or character string)
would you use to represent each of the following?  Try to come up with more than one good answer for each problem.  For example, in  # 1, when would counting days with a floating point variable make more sense than using an integer?

1. Number of days since the start of the year.
2. Time elapsed from the start of the year until now in days.
3. Serial number of a piece of lab equipment.
4. A lab specimen's age
5. Current population of a city.
6. Average population of a city over time.


## Division Types

In Python 3, the `//` operator performs integer (whole-number) floor division, the `/` operator performs floating-point
division, and the `%` (or *modulo*) operator calculates and returns the remainder from integer division:

```python
print('5 // 3:', 5 // 3)
print('5 / 3:', 5 / 3)
print('5 % 3:', 5 % 3)
```

```output
5 // 3: 1
5 / 3: 1.6666666666666667
5 % 3: 2
```

If `num_subjects` is the number of subjects taking part in a study,
and `num_per_survey` is the number that can take part in a single survey,
write an expression that calculates the number of surveys needed
to reach everyone once.


## Strings to Numbers

Where reasonable, `float()` will convert a string to a floating point number,
and `int()` will convert a floating point number to an integer:

```python
print("string to float:", float("3.4"))
print("float to int:", int(3.4))
```

```output
string to float: 3.4
float to int: 3
```

If the conversion doesn't make sense, however, an error message will occur.

```python
print("string to float:", float("Hello world!"))
```

```error
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-5-df3b790bf0a2> in <module>
----> 1 print("string to float:", float("Hello world!"))

ValueError: could not convert string to float: 'Hello world!'
```

Given this information, what do you expect the following program to do?

What does it actually do?

Why do you think it does that?

```python
print("fractional string to int:", int("3.4"))
```


## Arithmetic with Different Types

Which of the following will return the floating point number `2.0`?
Note: there may be more than one right answer.

```python
first = 1.0
second = "1"
third = "1.1"
```

1. `first + float(second)`
2. `float(second) + float(third)`
3. `first + int(third)`
4. `first + int(float(third))`
5. `int(first) + int(float(third))`
6. `2.0 * second`


## Complex Numbers

Python provides complex numbers,
which are written as `1.0+2.0j`.
If `val` is a complex number,
its real and imaginary parts can be accessed using *dot notation*
as `val.real` and `val.imag`.

```python
a_complex_number = 6 + 2j
print(a_complex_number.real)
print(a_complex_number.imag)
```

```output
6.0
2.0
```

1. Why do you think Python uses `j` instead of `i` for the imaginary part?
2. What do you expect `1 + 2j + 3` to produce?
3. What do you expect `4j` to be?  What about `4 j` or `4 + j`?

