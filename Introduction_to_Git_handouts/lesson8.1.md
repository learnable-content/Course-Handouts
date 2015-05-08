![](headers/Git Lesson 8.1.jpg)

# Introduction

In this lesson we'll be talking about a few ways to view your commit history in Git.

# Viewing Git Log

We've already worked with `git log` command that displays history of your commits with the author, date, hash or commit reference number and commit message.

You can also view your log by author which is useful if you're working in a team with other people. To do that, type

```
git log --author="name"
```

Just provide the name of the author (GitHub user name, for example).

To view your log tree, type

```
git log --graph --decorate --oneline
```

This shows you a history of your log tree on the left and the commit messages on the right. The `decorate` option lets you view the branch names and the `oneline` option lets you view everything on one line.

To limit the number of commits viewed, you can pass the option `n` (which stands for number) to the `git log` command:

```
git log -n 10
```

`git show` followed by a particular commit number will show you what lines in a particular file, or files, have changed for that specific commit.

Lastly, `git diff` will show you the differences between two branches:

```
git diff master featureA
```

This displays the differences between the `master` branch and the `featureA` branch.