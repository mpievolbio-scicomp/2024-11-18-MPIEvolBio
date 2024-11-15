
## Exploring More `ls` Options

You can also use two options at the same time. What does the command `ls` do when used
with the `-l` option? What about if you use both the `-l` and the `-h` option?

Some of its output is about properties that we do not cover in this lesson (such
as file permissions and ownership), but the rest should be useful
nevertheless.


## Listing in Reverse Chronological Order

By default, `ls` lists the contents of a directory in alphabetical
order by name. The command `ls -t` lists items by time of last
change instead of alphabetically. The command `ls -r` lists the
contents of a directory in reverse order.
Which file is displayed last when you combine the `-t` and `-r` options?
Hint: You may need to use the `-l` option to see the
last changed dates.


## Absolute vs Relative Paths

Starting from `/Users/nelle/data`,
which of the following commands could Nelle use to navigate to her home directory,
which is `/Users/nelle`?

1. `cd .`
2. `cd /`
3. `cd /home/nelle`
4. `cd ../..`
5. `cd ~`
6. `cd home`
7. `cd ~/data/..`
8. `cd`
9. `cd ..`




## `ls` Reading Comprehension

Using the filesystem diagram below,
if `pwd` displays `/Users/backup`,
and `-r` tells `ls` to display things in reverse order,
what command(s) will result in the following output:

```output
pnas_sub/ pnas_final/ original/
```


1. `ls pwd`
2. `ls -r -F`
3. `ls -r -F /Users/backup`

