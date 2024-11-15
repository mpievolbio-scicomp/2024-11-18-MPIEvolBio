
## Solving Conflicts that You Create

Clone the repository created by your instructor.
Add a new file to it,
and modify an existing file (your instructor will tell you which one).
When asked by your instructor,
pull her changes from the repository to create a conflict,
then resolve it.


::::::::::::::::::::::::::::::::::::::::::::::::::


## Conflicts on Non-textual files

What does Git do
when there is a conflict in an image or some other non-textual file
that is stored in version control?


## A Typical Work Session

You sit down at your computer to work on a shared project that is tracked in a
remote Git repository. During your work session, you take the following
actions, but not in this order:

- *Make changes* by appending the number `100` to a text file `numbers.txt`
- *Update remote* repository to match the local repository
- *Celebrate* your success with some fancy beverage(s)
- *Update local* repository to match the remote repository
- *Stage changes* to be committed
- *Commit changes* to the local repository

In what order should you perform these actions to minimize the chances of
conflicts? Put the commands above in order in the *action* column of the table
below. When you have the order right, see if you can write the corresponding
commands in the *command* column. A few steps are populated to get you
started.

| order | action . . . . . . . . . . | command . . . . . . . . . .                   | 
| ----- | -------------------------- | --------------------------------------------- |
| 1     |                            |                                               | 
| 2     |                            | `echo 100 >> numbers.txt`                     | 
| 3     |                            |                                               | 
| 4     |                            |                                               | 
| 5     |                            |                                               | 
| 6     | Celebrate!                 |                                               | 

