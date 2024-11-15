
## Fill in the Blanks

Fill in the blanks so that the program below produces the output shown.

```python
values = ____
values.____(1)
values.____(3)
values.____(5)
print('first time:', values)
values = values[____]
print('second time:', values)
```

```output
first time: [1, 3, 5]
second time: [3, 5]
```


## How Large is a Slice?

If `start` and `stop` are both non-negative integers,
how long is the list `values[start:stop]`?


## From Strings to Lists and Back

Given this:

```python
print('string to list:', list('tin'))
print('list to string:', ''.join(['g', 'o', 'l', 'd']))
```

```output
string to list: ['t', 'i', 'n']
list to string: gold
```

1. What does `list('some string')` do?
2. What does `'-'.join(['x', 'y', 'z'])` generate?


## Working With the End

What does the following program print?

```python
element = 'helium'
print(element[-1])
```

1. How does Python interpret a negative index?
2. If a list or string has N elements,
  what is the most negative index that can safely be used with it,
  and what location does that index represent?
3. If `values` is a list, what does `del values[-1]` do?
4. How can you display all elements but the last one without changing `values`?
  (Hint: you will need to combine slicing and negative indexing.)


## Stepping Through a List

What does the following program print?

```python
element = 'fluorine'
print(element[::2])
print(element[::-1])
```

1. If we write a slice as `low:high:stride`, what does `stride` do?
2. What expression would select all of the even-numbered items from a collection?


## Slice Bounds

What does the following program print?

```python
element = 'lithium'
print(element[0:20])
print(element[-1:3])
```


## Sort and Sorted

What do these two programs print?
In simple terms, explain the difference between `sorted(letters)` and `letters.sort()`.

```python
# Program A
letters = list('gold')
result = sorted(letters)
print('letters is', letters, 'and result is', result)
```

```python
# Program B
letters = list('gold')
result = letters.sort()
print('letters is', letters, 'and result is', result)
```


## Copying (or Not)

What do these two programs print?
In simple terms, explain the difference between `new = old` and `new = old[:]`.

```python
# Program A
old = list('gold')
new = old      # simple assignment
new[0] = 'D'
print('new is', new, 'and old is', old)
```

```python
# Program B
old = list('gold')
new = old[:]   # assigning a slice
new[0] = 'D'
print('new is', new, 'and old is', old)
```

