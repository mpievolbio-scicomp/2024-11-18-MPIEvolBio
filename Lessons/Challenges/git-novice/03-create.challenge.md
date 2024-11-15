
## Places to Create Git Repositories

Along with tracking information about recipes (the project we have already created),
Alfredo would also like to track information about desserts specifically.
Alfredo creates a `desserts` project inside his `recipes`
project with the following sequence of commands:

```bash
$ cd ~/Desktop    # return to Desktop directory
$ cd recipes      # go into recipes directory, which is already a Git repository
$ ls -a           # ensure the .git subdirectory is still present in the recipes directory
$ mkdir desserts # make a sub-directory recipes/desserts
$ cd desserts    # go into desserts subdirectory
$ git init        # make the desserts subdirectory a Git repository
$ ls -a           # ensure the .git subdirectory is present indicating we have created a new Git repository
```

Is the `git init` command, run inside the `desserts` subdirectory, required for
tracking files stored in the `desserts` subdirectory?

