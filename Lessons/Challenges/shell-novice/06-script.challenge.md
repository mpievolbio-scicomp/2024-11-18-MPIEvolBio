
## List Unique Species

Leah has several hundred data files, each of which is formatted like this:

```source
2013-11-05,deer,5
2013-11-05,rabbit,22
2013-11-05,raccoon,7
2013-11-06,rabbit,19
2013-11-06,deer,2
2013-11-06,fox,1
2013-11-07,rabbit,18
2013-11-07,bear,1
```

An example of this type of file is given in
`shell-lesson-data/exercise-data/animal-counts/animals.csv`.

We can use the command `cut -d , -f 2 animals.csv | sort | uniq` to produce
the unique species in `animals.csv`.
In order to avoid having to type out this series of commands every time,
a scientist may choose to write a shell script instead.

Write a shell script called `species.sh` that takes any number of
filenames as command-line arguments and uses a variation of the above command
to print a list of the unique species appearing in each of those files separately.


## Why Record Commands in the History Before Running Them?

If you run the command:

```bash
$ history | tail -n 5 > recent.sh
```

the last command in the file is the `history` command itself, i.e.,
the shell has added `history` to the command log before actually
running it. In fact, the shell *always* adds commands to the log
before running them. Why do you think it does this?


## Variables in Shell Scripts

In the `alkanes` directory, imagine you have a shell script called `script.sh` containing the
following commands:

```bash
head -n $2 $1
tail -n $3 $1
```

While you are in the `alkanes` directory, you type the following command:

```bash
$ bash script.sh '*.pdb' 1 1
```

Which of the following outputs would you expect to see?

1. All of the lines between the first and the last lines of each file ending in `.pdb`
  in the `alkanes` directory
2. The first and the last line of each file ending in `.pdb` in the `alkanes` directory
3. The first and the last line of each file in the `alkanes` directory
4. An error because of the quotes around `*.pdb`


## Find the Longest File With a Given Extension

Write a shell script called `longest.sh` that takes the name of a
directory and a filename extension as its arguments, and prints
out the name of the file with the most lines in that directory
with that extension. For example:

```bash
$ bash longest.sh shell-lesson-data/exercise-data/alkanes pdb
```

would print the name of the `.pdb` file in `shell-lesson-data/exercise-data/alkanes` that has
the most lines.

Feel free to test your script on another directory e.g.

```bash
$ bash longest.sh shell-lesson-data/exercise-data/writing txt
```


## Script Reading Comprehension

For this question, consider the `shell-lesson-data/exercise-data/alkanes` directory once again.
This contains a number of `.pdb` files in addition to any other files you
may have created.
Explain what each of the following three scripts would do when run as
`bash script1.sh *.pdb`, `bash script2.sh *.pdb`, and `bash script3.sh *.pdb` respectively.

```bash
# Script 1
echo *.*
```

```bash
# Script 2
for filename in $1 $2 $3
do
    cat $filename
done
```

```bash
# Script 3
echo $@.pdb
```


## Debugging Scripts

Suppose you have saved the following script in a file called `do-errors.sh`
in Nelle's `north-pacific-gyre` directory:

```bash
# Calculate stats for data files.
for datafile in "$@"
do
    echo $datfile
    bash goostats.sh $datafile stats-$datafile
done
```

When you run it from the `north-pacific-gyre` directory:

```bash
$ bash do-errors.sh NENE*A.txt NENE*B.txt
```

the output is blank.
To figure out why, re-run the script using the `-x` option:

```bash
$ bash -x do-errors.sh NENE*A.txt NENE*B.txt
```

What is the output showing you?
Which line is responsible for the error?

