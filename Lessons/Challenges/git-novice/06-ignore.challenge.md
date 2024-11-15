
## Ignoring Nested Files

Given a directory structure that looks like:

```bash
receipts/data
receipts/plots
```

How would you ignore only `receipts/plots` and not `receipts/data`?


## Including Specific Files

How would you ignore all `.png` files in your root directory except for
`final.png`?
Hint: Find out what `!` (the exclamation point operator) does


## Ignoring Nested Files: Variation

Given a directory structure that looks similar to the earlier Nested Files
exercise, but with a slightly different directory structure:

```bash
receipts/data
receipts/images
receipts/plots
receipts/analysis
```

How would you ignore all of the contents in the receipts folder, but not `receipts/data`?

Hint: think a bit about how you created an exception with the `!` operator
before.


## Ignoring all data Files in a Directory

Assuming you have an empty .gitignore file, and given a directory structure that looks like:

```bash
receipts/data/market_position/gps/a.dat
receipts/data/market_position/gps/b.dat
receipts/data/market_position/gps/c.dat
receipts/data/market_position/gps/info.txt
receipts/plots
```

What's the shortest `.gitignore` rule you could write to ignore all `.dat`
files in `result/data/market_position/gps`? Do not ignore the `info.txt`.


## Ignoring all data Files in the repository

Let us assume you have many `.csv` files in different subdirectories of your repository.
For example, you might have:

```bash
results/a.csv
data/experiment_1/b.csv
data/experiment_2/c.csv
data/experiment_2/variation_1/d.csv
```

How do you ignore all the `.csv` files, without explicitly listing the names of the corresponding folders?


## The Order of Rules

Given a `.gitignore` file with the following contents:

```bash
*.csv
!*.csv
```

What will be the result?


## Log Files

You wrote a script that creates many intermediate log-files of the form `log_01`, `log_02`, `log_03`, etc.
You want to keep them but you do not want to track them through `git`.

1. Write **one** `.gitignore` entry that excludes files of the form `log_01`, `log_02`, etc.

2. Test your "ignore pattern" by creating some dummy files of the form `log_01`, etc.

3. You find that the file `log_01` is very important after all, add it to the tracked files without changing the `.gitignore` again.

4. Discuss with your neighbor what other types of files could reside in your directory that you do not want to track and thus would exclude via `.gitignore`.

