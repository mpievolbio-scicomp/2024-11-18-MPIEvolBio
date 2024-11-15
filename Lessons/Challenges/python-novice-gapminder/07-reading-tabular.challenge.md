
## Reading Other Data

Read the data in `gapminder_gdp_americas.csv`
(which should be in the same directory as `gapminder_gdp_oceania.csv`)
into a variable called `data_americas`
and display its summary statistics.


## Inspecting Data

After reading the data for the Americas,
use `help(data_americas.head)` and `help(data_americas.tail)`
to find out what `DataFrame.head` and `DataFrame.tail` do.

1. What method call will display the first three rows of this data?
2. What method call will display the last three columns of this data?
  (Hint: you may need to change your view of the data.)


## Reading Files in Other Directories

The data for your current project is stored in a file called `microbes.csv`,
which is located in a folder called `field_data`.
You are doing analysis in a notebook called `analysis.ipynb`
in a sibling folder called `thesis`:

```output
your_home_directory
+-- field_data/
|   +-- microbes.csv
+-- thesis/
    +-- analysis.ipynb
```

What value(s) should you pass to `read_csv` to read `microbes.csv` in `analysis.ipynb`?


## Writing Data

As well as the `read_csv` function for reading data from a file,
Pandas provides a `to_csv` function to write dataframes to files.
Applying what you've learned about reading from files,
write one of your dataframes to a file called `processed.csv`.
You can use `help` to get information on how to use `to_csv`.

