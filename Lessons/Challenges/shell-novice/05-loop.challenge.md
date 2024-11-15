
## Write your own loop

How would you write a loop that echoes all 10 numbers from 0 to 9?


## Variables in Loops

This exercise refers to the `shell-lesson-data/exercise-data/alkanes` directory.
`ls *.pdb` gives the following output:

```output
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
```

What is the output of the following code?

```bash
$ for datafile in *.pdb
> do
>     ls *.pdb
> done
```

Now, what is the output of the following code?

```bash
$ for datafile in *.pdb
> do
>     ls $datafile
> done
```

Why do these two loops give different outputs?


## Limiting Sets of Files

What would be the output of running the following loop in the
`shell-lesson-data/exercise-data/alkanes` directory?

```bash
$ for filename in c*
> do
>     ls $filename
> done
```

1. No files are listed.
2. All files are listed.
3. Only `cubane.pdb`, `octane.pdb` and `pentane.pdb` are listed.
4. Only `cubane.pdb` is listed.


## Saving to a File in a Loop - Part One

In the `shell-lesson-data/exercise-data/alkanes` directory, what is the effect of this loop?

```bash
for alkanes in *.pdb
do
    echo $alkanes
    cat $alkanes > alkanes.pdb
done
```

1. Prints `cubane.pdb`, `ethane.pdb`, `methane.pdb`, `octane.pdb`, `pentane.pdb` and
  `propane.pdb`, and the text from `propane.pdb` will be saved to a file called `alkanes.pdb`.
2. Prints `cubane.pdb`, `ethane.pdb`, and `methane.pdb`, and the text from all three files
  would be concatenated and saved to a file called `alkanes.pdb`.
3. Prints `cubane.pdb`, `ethane.pdb`, `methane.pdb`, `octane.pdb`, and `pentane.pdb`,
  and the text from `propane.pdb` will be saved to a file called `alkanes.pdb`.
4. None of the above.


## Saving to a File in a Loop - Part Two

Also in the `shell-lesson-data/exercise-data/alkanes` directory,
what would be the output of the following loop?

```bash
for datafile in *.pdb
do
    cat $datafile >> all.pdb
done
```

1. All of the text from `cubane.pdb`, `ethane.pdb`, `methane.pdb`, `octane.pdb`, and
  `pentane.pdb` would be concatenated and saved to a file called `all.pdb`.
2. The text from `ethane.pdb` will be saved to a file called `all.pdb`.
3. All of the text from `cubane.pdb`, `ethane.pdb`, `methane.pdb`, `octane.pdb`, `pentane.pdb`
  and `propane.pdb` would be concatenated and saved to a file called `all.pdb`.
4. All of the text from `cubane.pdb`, `ethane.pdb`, `methane.pdb`, `octane.pdb`, `pentane.pdb`
  and `propane.pdb` would be printed to the screen and saved to a file called `all.pdb`.


## Doing a Dry Run

A loop is a way to do many things at once --- or to make many mistakes at
once if it does the wrong thing. One way to check what a loop *would* do
is to `echo` the commands it would run instead of actually running them.

Suppose we want to preview the commands the following loop will execute
without actually running those commands:

```bash
$ for datafile in *.pdb
> do
>     cat $datafile >> all.pdb
> done
```

What is the difference between the two loops below, and which one would we
want to run?

```bash
# Version 1
$ for datafile in *.pdb
> do
>     echo cat $datafile >> all.pdb
> done
```

```bash
# Version 2
$ for datafile in *.pdb
> do
>     echo "cat $datafile >> all.pdb"
> done
```


## Nested Loops

Suppose we want to set up a directory structure to organize
some experiments measuring reaction rate constants with different compounds
*and* different temperatures.  What would be the
result of the following code:

```bash
$ for species in cubane ethane methane
> do
>     for temperature in 25 30 37 40
>     do
>         mkdir $species-$temperature
>     done
> done
```

