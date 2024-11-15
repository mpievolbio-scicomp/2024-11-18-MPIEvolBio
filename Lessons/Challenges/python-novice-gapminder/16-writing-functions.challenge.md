
## Identifying Syntax Errors

1. Read the code below and try to identify what the errors are
  *without* running it.
2. Run the code and read the error message.
  Is it a `SyntaxError` or an `IndentationError`?
3. Fix the error.
4. Repeat steps 2 and 3 until you have fixed all the errors.

```python
def another_function
  print("Syntax errors are annoying.")
   print("But at least python tells us about them!")
  print("So they are usually not too hard to fix.")
```


## Definition and Use

What does the following program print?

```python
def report(pressure):
    print('pressure is', pressure)

print('calling', report, 22.5)
```


## Order of Operations

1. What's wrong in this example?
  
  ```python
  result = print_time(11, 37, 59)
  
  def print_time(hour, minute, second):
     time_string = str(hour) + ':' + str(minute) + ':' + str(second)
     print(time_string)
  ```

2. After fixing the problem above, explain why running this example code:
  
  ```python
  result = print_time(11, 37, 59)
  print('result of call is:', result)
  ```
  
  gives this output:
  
  ```output
  11:37:59
  result of call is: None
  ```

3. Why is the result of the call `None`?


## Encapsulation

Fill in the blanks to create a function that takes a single filename as an argument,
loads the data in the file named by the argument,
and returns the minimum value in that data.

```python
import pandas as pd

def min_in_data(____):
    data = ____
    return ____
```


## Find the First

Fill in the blanks to create a function that takes a list of numbers as an argument
and returns the first negative value in the list.
What does your function do if the list is empty? What if the list has no negative numbers?

```python
def first_negative(values):
    for v in ____:
        if ____:
            return ____
```


## Calling by Name

Earlier we saw this function:

```python
def print_date(year, month, day):
    joined = str(year) + '/' + str(month) + '/' + str(day)
    print(joined)
```

We saw that we can call the function using *named arguments*, like this:

```python
print_date(day=1, month=2, year=2003)
```

1. What does `print_date(day=1, month=2, year=2003)` print?
2. When have you seen a function call like this before?
3. When and why is it useful to call functions this way?


## Encapsulation of an If/Print Block

The code below will run on a label-printer for chicken eggs.  A digital scale will report a chicken egg mass (in grams)
to the computer and then the computer will print a label.

```python
import random
for i in range(10):

    # simulating the mass of a chicken egg
    # the (random) mass will be 70 +/- 20 grams
    mass = 70 + 20.0 * (2.0 * random.random() - 1.0)

    print(mass)

    # egg sizing machinery prints a label
    if mass >= 85:
        print("jumbo")
    elif mass >= 70:
        print("large")
    elif mass < 70 and mass >= 55:
        print("medium")
    else:
        print("small")
```

The if-block that classifies the eggs might be useful in other situations,
so to avoid repeating it, we could fold it into a function, `get_egg_label()`.
Revising the program to use the function would give us this:

```python
# revised version
import random
for i in range(10):

    # simulating the mass of a chicken egg
    # the (random) mass will be 70 +/- 20 grams
    mass = 70 + 20.0 * (2.0 * random.random() - 1.0)

    print(mass, get_egg_label(mass))

```

1. Create a function definition for `get_egg_label()` that will work with the revised program above.  Note that the `get_egg_label()` function's return value will be important. Sample output from the above program would be `71.23 large`.
2. A dirty egg might have a mass of more than 90 grams, and a spoiled or broken egg will probably have a mass that's less than 50 grams.  Modify your `get_egg_label()` function to account for these error conditions. Sample output could be `25 too light, probably spoiled`.


## Encapsulating Data Analysis

Assume that the following code has been executed:

```python
import pandas as pd

data_asia = pd.read_csv('data/gapminder_gdp_asia.csv', index_col=0)
japan = data_asia.loc['Japan']
```

1. Complete the statements below to obtain the average GDP for Japan
  across the years reported for the 1980s.
  
  ```python
  year = 1983
  gdp_decade = 'gdpPercap_' + str(year // ____)
  avg = (japan.loc[gdp_decade + ___] + japan.loc[gdp_decade + ___]) / 2
  ```

2. Abstract the code above into a single function.
  
  ```python
  def avg_gdp_in_decade(country, continent, year):
      data_countries = pd.read_csv('data/gapminder_gdp_'+___+'.csv',delimiter=',',index_col=0)
      ____
      ____
      ____
      return avg
  ```

3. How would you generalize this function
  if you did not know beforehand which specific years occurred as columns in the data?
  For instance, what if we also had data from years ending in 1 and 9 for each decade?
  (Hint: use the columns to filter out the ones that correspond to the decade,
  instead of enumerating them in the code.)


## Simulating a dynamical system

In mathematics, a [dynamical system](https://en.wikipedia.org/wiki/Dynamical_system) is a system
in which a function describes the time dependence of a point in a geometrical space. A canonical
example of a dynamical system is the [logistic map](https://en.wikipedia.org/wiki/Logistic_map),
a growth model that computes a new population density (between  0 and 1) based on the current
density. In the model, time takes discrete values 0, 1, 2, ...

1. Define a function called `logistic_map` that takes two inputs: `x`, representing the current
  population (at time `t`), and a parameter `r = 1`. This function should return a value
  representing the state of the system (population) at time `t + 1`, using the mapping function:
  
  `f(t+1) = r * f(t) * [1 - f(t)]`

2. Using a `for` or `while` loop, iterate the `logistic_map` function defined in part 1, starting
  from an initial population of 0.5, for a period of time `t_final = 10`. Store the intermediate
  results in a list so that after the loop terminates you have accumulated a sequence of values
  representing the state of the logistic map at times `t = [0,1,...,t_final]` (11 values in total).
  Print this list to see the evolution of the population.

3. Encapsulate the logic of your loop into a function called `iterate` that takes the initial
  population as its first input, the parameter `t_final` as its second input and the parameter
  `r` as its third input. The function should return the list of values representing the state of
  the logistic map at times `t = [0,1,...,t_final]`. Run this function for periods `t_final = 100`
  and `1000` and print some of the values. Is the population trending toward a steady state?

