# Creating a New Branch
```sh
$ git branch <branch_name>
```

# Switching Branch
```sh
$ git checkout <branch_name>

# Alternate way
$ git switch <branch_name>
```

- Creating a new branch and immediately switching to that branch
```sh
$ git checkout -b <branch_name>

# Alternate way
$ git switch -c <branch_name>
```

# Merge Branch
- Switch to the branch you want other branches to merge into.
- Run the `git merge` command and specify the branch you want to merge from.

**Example :** Merging branch iss450 into master.
```sh
$ git checkout master
$ git merge iss450
```

- Type of merges : 
    - **Fast forward merge.**
    - **Three way merge.**

- Sometimes during merging of branches some merege confict arises, without resolving those conflicts we cannot move further.

# Delete a Branch

```sh
$ git branch -d <branch_name>
```

# Branch Management
`--merged` and `--no-merged` options can filter this list to branches that you have or have not yet merged into the branch you’re currently on.

```sh
$ git branch --merged

$ git branch --no-merged
```

# Changing Branch Name
```sh
$ git branch --move old-branch-name new-branch-name
```
This will only change the local branch name. To change the remote branch name as well :
```sh
$ git push --set-upstream origin new-branch-name
```

However, the branch with the old name is also still present there but you can delete it by executing the following command:
```sh
$ git push origin --delete old-branch-name
```

