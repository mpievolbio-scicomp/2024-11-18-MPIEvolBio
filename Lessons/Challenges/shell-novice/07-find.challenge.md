
## Using `grep`

Which command would result in the following output:

```output
and the presence of absence:
```

1. `grep "of" haiku.txt`
2. `grep -E "of" haiku.txt`
3. `grep -w "of" haiku.txt`
4. `grep -i "of" haiku.txt`


## Tracking a Species

Leah has several hundred
data files saved in one directory, each of which is formatted like this:

```source
2012-11-05,deer,5
2012-11-05,rabbit,22
2012-11-05,raccoon,7
2012-11-06,rabbit,19
2012-11-06,deer,2
2012-11-06,fox,4
2012-11-07,rabbit,16
2012-11-07,bear,1
```

She wants to write a shell script that takes a species as the first command-line argument
and a directory as the second argument. The script should return one file called `<species>.txt`
containing a list of dates and the number of that species seen on each date.
For example using the data shown above, `rabbit.txt` would contain:

```source
2012-11-05,22
2012-11-06,19
2012-11-07,16
```

Below, each line contains an individual command, or pipe.  Arrange their
sequence in one command in order to achieve Leah's goal:

```bash
cut -d : -f 2
>
|
grep -w $1 -r $2
|
$1.txt
cut -d , -f 1,3
```

Hint: use `man grep` to look for how to grep text recursively in a directory
and `man cut` to select more than one field in a line.

An example of such a file is provided in
`shell-lesson-data/exercise-data/animal-counts/animals.csv`


## Little Women

You and your friend, having just finished reading *Little Women* by
Louisa May Alcott, are in an argument.  Of the four sisters in the
book, Jo, Meg, Beth, and Amy, your friend thinks that Jo was the
most mentioned.  You, however, are certain it was Amy.  Luckily, you
have a file `LittleWomen.txt` containing the full text of the novel
(`shell-lesson-data/exercise-data/writing/LittleWomen.txt`).
Using a `for` loop, how would you tabulate the number of times each
of the four sisters is mentioned?


## Matching and Subtracting

The `-v` option to `grep` inverts pattern matching, so that only lines
which do *not* match the pattern are printed. Given that, which of
the following commands will find all .dat files in `creatures`
except `unicorn.dat`?
Once you have thought about your answer, you can test the commands in the
`shell-lesson-data/exercise-data` directory.

1. `find creatures -name "*.dat" | grep -v unicorn`
2. `find creatures -name *.dat | grep -v unicorn`
3. `grep -v "unicorn" $(find creatures -name "*.dat")`
4. None of the above.


## `find` Pipeline Reading Comprehension

Write a short explanatory comment for the following shell script:

```bash
wc -l $(find . -name "*.dat") | sort -n
```

