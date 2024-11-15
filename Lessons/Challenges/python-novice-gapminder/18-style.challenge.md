
## What Will Be Shown?

Highlight the lines in the code below that will be available as online help.
Are there lines that should be made available, but won't be?
Will any lines produce a syntax error or a runtime error?

```python
"Find maximum edit distance between multiple sequences."
# This finds the maximum distance between all sequences.

def overall_max(sequences):
    '''Determine overall maximum edit distance.'''

    highest = 0
    for left in sequences:
        for right in sequences:
            '''Avoid checking sequence against itself.'''
            if left != right:
                this = edit_distance(left, right)
                highest = max(highest, this)

    # Report.
    return highest
```

::::::::::::::::::::::::::::::::::::::::::::::::::


## Document This

Use comments to describe and help others understand potentially unintuitive
sections or individual lines of code. They are especially useful to whoever
may need to understand and edit your code in the future, including yourself.

Use docstrings to document the acceptable inputs and expected outputs of a method
or class, its purpose, assumptions and intended behavior. Docstrings are displayed
when a user invokes the builtin `help` method on your method or class.

Turn the comment in the following function into a docstring
and check that `help` displays it properly.

```python
def middle(a, b, c):
    # Return the middle value of three.
    # Assumes the values can actually be compared.
    values = [a, b, c]
    values.sort()
    return values[1]
```


## Clean Up This Code

1. Read this short program and try to predict what it does.
2. Run it: how accurate was your prediction?
3. Refactor the program to make it more readable.
  Remember to run it after each change to ensure its behavior hasn't changed.
4. Compare your rewrite with your neighbor's.
  What did you do the same?
  What did you do differently, and why?

```python
n = 10
s = 'et cetera'
print(s)
i = 0
while i < n:
    # print('at', j)
    new = ''
    for j in range(len(s)):
        left = j-1
        right = (j+1)%len(s)
        if s[left]==s[right]: new = new + '-'
        else: new = new + '*'
    s=''.join(new)
    print(s)
    i += 1
```

