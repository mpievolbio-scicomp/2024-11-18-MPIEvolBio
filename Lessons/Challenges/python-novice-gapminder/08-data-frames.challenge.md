
## Selection of Individual Values

Assume Pandas has been imported into your notebook
and the Gapminder GDP data for Europe has been loaded:

```python
import pandas as pd

data_europe = pd.read_csv('data/gapminder_gdp_europe.csv', index_col='country')
```

Write an expression to find the Per Capita GDP of Serbia in 2007.


## Extent of Slicing

1. Do the two statements below produce the same output?
2. Based on this,
  what rule governs what is included (or not) in numerical slices and named slices in Pandas?

```python
print(data_europe.iloc[0:2, 0:2])
print(data_europe.loc['Albania':'Belgium', 'gdpPercap_1952':'gdpPercap_1962'])
```


## Reconstructing Data

Explain what each line in the following short program does:
what is in `first`, `second`, etc.?

```python
first = pd.read_csv('data/gapminder_all.csv', index_col='country')
second = first[first['continent'] == 'Americas']
third = second.drop('Puerto Rico')
fourth = third.drop('continent', axis = 1)
fourth.to_csv('result.csv')
```


## Selecting Indices

Explain in simple terms what `idxmin` and `idxmax` do in the short program below.
When would you use these methods?

```python
data = pd.read_csv('data/gapminder_gdp_europe.csv', index_col='country')
print(data.idxmin())
print(data.idxmax())
```


## Practice with Selection

Assume Pandas has been imported and the Gapminder GDP data for Europe has been loaded.
Write an expression to select each of the following:

1. GDP per capita for all countries in 1982.
2. GDP per capita for Denmark for all years.
3. GDP per capita for all countries for years *after* 1985.
4. GDP per capita for each country in 2007 as a multiple of
  GDP per capita for that country in 1952.


## Many Ways of Access

There are at least two ways of accessing a value or slice of a DataFrame: by name or index.
However, there are many others. For example, a single column or row can be accessed either as a `DataFrame`
or a `Series` object.

Suggest different ways of doing the following operations on a DataFrame:

1. Access a single column
2. Access a single row
3. Access an individual DataFrame element
4. Access several columns
5. Access several rows
6. Access a subset of specific rows and columns
7. Access a subset of row and column ranges


## Exploring available methods using the `dir()` function

Python includes a `dir()` function that can be used to display all of the available methods (functions) that are built into a data object.  In Episode 4, we used some methods with a string. But we can see many more are available by using `dir()`:

```python
my_string = 'Hello world!'   # creation of a string object 
dir(my_string)
```

This command returns:

```python
['__add__',
...
'__subclasshook__',
'capitalize',
'casefold',
'center',
...
'upper',
'zfill']
```

You can use `help()` or <kbd>Shift</kbd>\+<kbd>Tab</kbd> to get more information about what these methods do.

Assume Pandas has been imported and the Gapminder GDP data for Europe has been loaded as `data`.  Then, use `dir()`
to find the function that prints out the median per-capita GDP across all European countries for each year that information is available.


## Interpretation

Poland's borders have been stable since 1945,
but changed several times in the years before then.
How would you handle this if you were creating a table of GDP per capita for Poland
for the entire twentieth century?


::::::::::::::::::::::::::::::::::::::::::::::::::

[pandas-dataframe]: https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.html
[pandas-series]: https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.html
[numpy]: https://www.numpy.org/


:::::::::::::::::::::::::::::::::::::::: keypoints

- Use `DataFrame.iloc[..., ...]` to select values by integer location.
- Use `:` on its own to mean all columns or all rows.
- Select multiple columns or rows using `DataFrame.loc` and a named slice.
- Result of slicing can be used in further operations.
- Use comparisons to select data based on value.
- Select values or NaN using a Boolean mask.

::::::::::::::::::::::::::::::::::::::::::::::::::


