![](headers/Git Lesson 5.1.jpg)

# Introduction

In this lesson, we'll talk about making mistakes at each step of the workflow that we just created. We'll be making three deliberate mistakes to the items after our carousel. These three mistakes will be part of the three commands that you just learned: `git add`, `git commit`, and `git push`. So for the first part, we'll learn how to undo mistakes after you add it to the staging area.

# Undoing a change

Open *index.html* in the cod editor and replace "Welcome to" with

```html
<small>Our First Mistake!</small>
```

In your terminal run

```
git status
```

command which tells us that *index.html* has been changed as expected.

Let's add our mistake to the staging area

```
git add index.html
```

So, suppose you added something to the staging area, which isn't supposed to be there. How do you then unstage it from the staging area? To do that, type in

```
git reset HEAD index.html
```

This will reset your staging area and remove any files from there.

Type in

```
git status
```

This confirms that *index.html* was in fact removed from the staging area. You've unstaged the file from the staging area, but your error still exists in the *index.html* file, and you have to manually fix that.