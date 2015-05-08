![](headers/Git Lesson 7.12.jpg)

# Introduction

We're done merging our branches, so now let's tidy them up.

# Deleting Branches

In your terminal type

```
git branch -a
```

This lists all the branches that we have locally and our remote branches.

Let's delete the `featureC` branch first:

```
git branch -d featureC
```

Now delete `featureB`

```
git branch -d featureB
```

Now delete the remote `featureB` branch with

```
git push origin --delete featureB
```

Congratulations, you've completed a chunk of the project!