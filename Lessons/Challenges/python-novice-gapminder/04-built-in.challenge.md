
## What Happens When

1. Explain in simple terms the order of operations in the following program:
  when does the addition happen, when does the subtraction happen,
  when is each function called, etc.
2. What is the final value of `radiance`?

```python
radiance = 1.0
radiance = max(2.1, 2.0 + min(radiance, 1.1 * radiance - 0.5))
```


## Spot the Difference

1. Predict what each of the `print` statements in the program below will print.
2. Does `max(len(rich), poor)` run or produce an error message?
  If it runs, does its result make any sense?

```python
easy_string = "abc"
print(max(easy_string))
rich = "gold"
poor = "tin"
print(max(rich, poor))
print(max(len(rich), len(poor)))
```


## Why Not?

Why is it that `max` and `min` do not return `None` when they are called with no arguments?


## Last Character of a String

If Python starts counting from zero,
and `len` returns the number of characters in a string,
what index expression will get the last character in the string `name`?
(Note: we will see a simpler way to do this in a later episode.)

