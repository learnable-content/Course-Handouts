![](headers/Git Lesson 5.2.jpg)

# Introduction

In this section we will add a file change to the staging area and commit it. Then I will show you how to undo a committed file change.

# Undoing a committed change

Replace "This Git Course" with

```html
<h1 class="brand-name">Our Second Mistake!</h1>
```

In the terminal type in

```
git add index.html
git commit -m "Committing our second mistake"
```

Type in

```
git log --pretty=oneline
```

In order to undo something you committed by mistake type in

```
git reset --soft HEAD~1
```

The `soft` option deletes the commit but leaves your files unchanged. The `HEAD~1` refers to the last commit before a mistake, so it resets the head to one commit prior to our mistake commit.

Now, typing

```
git status
```

assures us that *index.html* is still staged. Because we made a mistake, let's unstage the file

```
git reset HEAD index.html
```

Do

```
git status
```

which shows us that *index.html* isn't on the staging area.