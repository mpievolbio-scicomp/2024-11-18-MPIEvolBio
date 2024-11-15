
## Swapping Values

Fill the table showing the values of the variables in this program
*after* each statement is executed.

```python
# Command  # Value of x   # Value of y   # Value of swap #
x = 1.0    #              #              #               #
y = 3.0    #              #              #               #
swap = x   #              #              #               #
x = y      #              #              #               #
y = swap   #              #              #               #
```


## Predicting Values

What is the final value of `position` in the program below?
(Try to predict the value without running the program,
then check your prediction.)

```python
initial = 'left'
position = initial
initial = 'right'
```


## Challenge

If you assign `a = 123`,
what happens if you try to get the second digit of `a` via `a[1]`?


## Choosing a Name

Which is a better variable name, `m`, `min`, or `minutes`?
Why?
Hint: think about which code you would rather inherit
from someone who is leaving the lab:

1. `ts = m * 60 + s`
2. `tot_sec = min * 60 + sec`
3. `total_seconds = minutes * 60 + seconds`


## Slicing practice

What does the following program print?

```python
atom_name = 'carbon'
print('atom_name[1:3] is:', atom_name[1:3])
```


## Slicing concepts

Given the following string:

```python
species_name = "Acacia buxifolia"
```

What would these expressions return?

1. `species_name[2:8]`
2. `species_name[11:]` (without a value after the colon)
3. `species_name[:4]` (without a value before the colon)
4. `species_name[:]` (just a colon)
5. `species_name[11:-3]`
6. `species_name[-5:-3]`
7. What happens when you choose a `stop` value which is out of range? (i.e., try `species_name[0:20]` or `species_name[:103]`)

