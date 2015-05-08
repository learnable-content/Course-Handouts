![](headers/Git Lesson 6.2.jpg)

# Introduction

There's an easier way of fetching and merging remote changes into your local repo using the `git pull` command.

# Merging changes with Git pull

The `git pull` command combines both `git fetch` and `git merge`, so it will fetch and merge the latest commit on the GitHub repo into your local repo.

Go to GitHub and make another edit to *readme*: "Third edit by Lara". Commit it with a message "third edit by Lara".

Come back to the terminal, and type in

```
git pull origin master
```

This pulls changes from the remote repo called origin into the local master branch of your repo. Open *readme* file - it should contain all the recent changes.