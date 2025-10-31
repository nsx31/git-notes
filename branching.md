# Creating a New Branch
```sh
$ git branch <branch_name>
```

# Switching Branch
```sh
$ git checkout <branch_name>
```

Creating a new branch and immediately switching to that branch
```sh
$ git checkout -b <branch_name>
```

# Merge Branch
- First switch to the branch you want other branch to merge into.

Example : Merging branch iss450 into master.
```sh
$ git checkout master
$ git merge iss450
```
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

