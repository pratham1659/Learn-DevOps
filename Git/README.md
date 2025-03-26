# Chapter 2 - Git Fundamentals

Here are some basic **Git commands** you should know:

- Git status - To check for any change in the repo

- Git diff - To see the difference of current version with last
  committed version

- Git pull - To fetch the latest files from remote repo

- Git add - To add the modified files in staging area

- Git commit - To add the changes in git repo

- Git push - To push the committed changes in Remote repo

- Git log - To see the old commits history
- Git clone - To clone the repo in system

### How to Revert Changes

```
git restore filename
```

### How to check Git Cache

```
git diff -- cached
```

```
git restore --worktree
```

```
git reset --soft HEAD^
git reset --hard HEAD^
```

```
git log -p -2 (last two commit with diff)
git log --stat (summary of changes)

git log --pretty=oneline
git log --pretty=format:"%h - %an, %ar : %s"

git log -S "realted_word"

git log --grep="V"
git log --grep="fix bug" (search commit msg)

git log --since="2024-01-01"
git log --until="2024-01-01"

git log --author="Paul"
git log --no-merges
```

```
git checkout main
git branch


git branch new_branch
```

#### A remote repository refers to a version of your project that resides on a network server or a hosted repository on the internet.

```
git remote
git remote -v
```

### Git Branching and Merging

```
git merge design
```

#### How to Clean untracked files in Git

```
git clean -n
git clean -f
```

#### How to add tag in particular commits in Git

```
git tag -a "readme" -m "This is Readme Commit

git show readme

// To create annotated tags
git tag -a v1.0 -m "My version 1.0"

//To show tags data
git show v1.0

//To tag old commit in case you forgot
git tag -a v1.2 < commit_no>


git push origin --tags
```
