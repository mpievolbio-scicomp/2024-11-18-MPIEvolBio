
## Classifying Errors

Is an indentation error a syntax error or a runtime error?


## Tracing Execution

Create a table showing the numbers of the lines that are executed when this program runs,
and the values of the variables after each line is executed.

```python
total = 0
for char in "tin":
    total = total + 1
```


## Reversing a String

Fill in the blanks in the program below so that it prints "nit"
(the reverse of the original character string "tin").

```python
original = "tin"
result = ____
for char in original:
    result = ____
print(result)
```


## Practice Accumulating

Fill in the blanks in each of the programs below
to produce the indicated result.

```python
# Total length of the strings in the list: ["red", "green", "blue"] => 12
total = 0
for word in ["red", "green", "blue"]:
    ____ = ____ + len(word)
print(total)
```


## Cumulative Sum

Reorder and properly indent the lines of code below
so that they print a list with the cumulative sum of data.
The result should be `[1, 3, 5, 10]`.

```python
cumulative.append(total)
for number in data:
cumulative = []
total = total + number
total = 0
print(cumulative)
data = [1,2,2,5]
```


## Identifying Variable Name Errors

1. Read the code below and try to identify what the errors are
  *without* running it.
2. Run the code and read the error message.
  What type of `NameError` do you think this is?
  Is it a string with no quotes, a misspelled variable, or a
  variable that should have been defined but was not?
3. Fix the error.
4. Repeat steps 2 and 3, until you have fixed all the errors.

```python
for number in range(10):
    # use a if the number is a multiple of 3, otherwise use b
    if (Number % 3) == 0:
        message = message + a
    else:
        message = message + "b"
print(message)
```


## Identifying Item Errors

1. Read the code below and try to identify what the errors are
  *without* running it.
2. Run the code, and read the error message. What type of error is it?
3. Fix the error.

```python
seasons = ['Spring', 'Summer', 'Fall', 'Winter']
print('My favorite season is ', seasons[4])
```

