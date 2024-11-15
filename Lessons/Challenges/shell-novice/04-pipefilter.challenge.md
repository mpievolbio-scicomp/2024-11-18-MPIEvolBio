
## What Does `sort -n` Do?

The file `shell-lesson-data/exercise-data/numbers.txt` contains the following lines:

```source
10
2
19
22
6
```

If we run `sort` on this file, the output is:

```output
10
19
2
22
6
```

If we run `sort -n` on the same file, we get this instead:

```output
2
6
10
19
22
```

Explain why `-n` has this effect.


## What Does `>>` Mean?

We have seen the use of `>`, but there is a similar operator `>>`
which works slightly differently.
We'll learn about the differences between these two operators by printing some strings.
We can use the `echo` command to print strings e.g.

```bash
$ echo The echo command prints text
```

```output
The echo command prints text
```

Now test the commands below to reveal the difference between the two operators:

```bash
$ echo hello > testfile01.txt
```

and:

```bash
$ echo hello >> testfile02.txt
```

Hint: Try executing each command twice in a row and then examining the output files.


## Appending Data

We have already met the `head` command, which prints lines from the start of a file.
`tail` is similar, but prints lines from the end of a file instead.

Consider the file `shell-lesson-data/exercise-data/animal-counts/animals.csv`.
After these commands, select the answer that
corresponds to the file `animals-subset.csv`:

```bash
$ head -n 3 animals.csv > animals-subset.csv
$ tail -n 2 animals.csv >> animals-subset.csv
```

1. The first three lines of `animals.csv`
2. The last two lines of `animals.csv`
3. The first three lines and the last two lines of `animals.csv`
4. The second and third lines of `animals.csv`


## Piping Commands Together

In our current directory, we want to find the 3 files which have the least number of
lines. Which command listed below would work?

1. `wc -l * > sort -n > head -n 3`
2. `wc -l * | sort -n | head -n 1-3`
3. `wc -l * | head -n 3 | sort -n`
4. `wc -l * | sort -n | head -n 3`


## Pipe Reading Comprehension

A file called `animals.csv` (in the `shell-lesson-data/exercise-data/animal-counts` folder)
contains the following data:

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

What text passes through each of the pipes and the final redirect in the pipeline below?
Note, the `sort -r` command sorts in reverse order.

```bash
$ cat animals.csv | head -n 5 | tail -n 3 | sort -r > final.txt
```

Hint: build the pipeline up one command at a time to test your understanding


## Pipe Construction

For the file `animals.csv` from the previous exercise, consider the following command:

```bash
$ cut -d , -f 2 animals.csv
```

The `cut` command is used to remove or 'cut out' certain sections of each line in the file,
and `cut` expects the lines to be separated into columns by a <kbd>Tab</kbd> character.
A character used in this way is called a **delimiter**.
In the example above we use the `-d` option to specify the comma as our delimiter character.
We have also used the `-f` option to specify that we want to extract the second field (column).
This gives the following output:

```output
deer
rabbit
raccoon
rabbit
deer
fox
rabbit
bear
```

The `uniq` command filters out adjacent matching lines in a file.
How could you extend this pipeline (using `uniq` and another command) to find
out what animals the file contains (without any duplicates in their
names)?


## Which Pipe?

The file `animals.csv` contains 8 lines of data formatted as follows:

```output
2012-11-05,deer,5
2012-11-05,rabbit,22
2012-11-05,raccoon,7
2012-11-06,rabbit,19
...
```

The `uniq` command has a `-c` option which gives a count of the
number of times a line occurs in its input.  Assuming your current
directory is `shell-lesson-data/exercise-data/animal-counts`,
what command would you use to produce a table that shows
the total count of each type of animal in the file?

1. `sort animals.csv | uniq -c`
2. `sort -t, -k2,2 animals.csv | uniq -c`
3. `cut -d, -f 2 animals.csv | uniq -c`
4. `cut -d, -f 2 animals.csv | sort | uniq -c`
5. `cut -d, -f 2 animals.csv | sort | uniq -c | wc -l`


## Removing Unneeded Files

Suppose you want to delete your processed data files, and only keep
your raw files and processing script to save storage.
The raw files end in `.dat` and the processed files end in `.txt`.
Which of the following would remove all the processed data files,
and *only* the processed data files?

1. `rm ?.txt`
2. `rm *.txt`
3. `rm * .txt`
4. `rm *.*`

