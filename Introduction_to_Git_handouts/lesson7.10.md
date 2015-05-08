![](headers/Git Lesson 7.10.jpg)

# Merging Branch featureB into Branch featureA

Now we're going to merge the `featureB` branch into the `featureA` branch.

Check out into the `featureA` branch with

```
git checkout featureA
```

To merge the `featureB` branch into `featureA` type

```
git merge featureB
```

Even though we didn't specify it to be a no fast-forward merge, it's still asking us to write a merge commit message. This is because development has taken place in both branches ever since we made them, and a three way merge is utilized.

You can check commits using

```
git log --pretty=oneline
```