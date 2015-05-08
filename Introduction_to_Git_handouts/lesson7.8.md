![](headers/Git Lesson 7.8.jpg)

# Introduction

In this section we'll work on our local `featureC` branch, which has no work on it so far, and merge it into a master branch using a fast forward merge.

# Using Fast forward merge

In your terminal, type

```
git checkout featureC
```

Open your code editor and scroll down to the bottom where the `footer` tag is located. Replace the text inside the `p` tags

```html
<p>Git 2015</p>
```

Come back to the terminal and add *index.html* file to the staging area with

```
git add index.html
```

Next, commit the file change with

```
git commit -m "Changed text inside footer"
```

Let's perform the first step of merging our `featureC` branch into `master`:

```
git checkout master
```

To merge the `featureC` branch into `master` type

```
git merge featureC
```

Merge will be done by a fast forward - this means that there was a linear path from the `master` branch to the `featureC` branch since no development occurred on `master` after we made our `featureC` branch.

So, all Git did was moving the current branch tip, which is called HEAD, on `master`, to the target branch tip on the `featureC` branch.

Run

```
git log dash --pretty=oneline
```

You will see that the second most recent commit on `master` is when we decided to keep our color instead of Lara's, whereas the latest commit on `master` now is what we committed on our `featureC` branch.