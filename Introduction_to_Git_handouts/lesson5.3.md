![](headers/Git Lesson 5.3.jpg)

# Introduction

At this step we will add, commit and push our mistake to the repository on GitHub.

# Undoing a pushed change

Replace "Kauress" with

```html
<strong>Start Bootstrap</strong>
```

Add our file change to the staging area with

```
git add index.html
```

Commit the file change with

```
git commit -m "Committing our third mistake, we left the other two in place"
```

Typing in

```
git log --pretty=oneline
```

we can see the Git commit and it's message. Press `Q` to exit.

Now push our mistake over to GitHub with

```
git push origin master
```

How do we undo that? Type in

```
git revert HEAD
```

This opens up the default editor for your terminal, where we can type in a commit message. Let this be as is, and exit the editor.

What `git revert HEAD` does is creating a separate revert commit, which points to the commit before you committed your mistake.

To check this run

```
git log --pretty=oneline
```

You can see the revert commit that was created by `git revert HEAD` command.

Open *index.html* file in the code editor and note that the third error is gone. However, on GitHub nothing has changed, our mistake is still there. This is because even though we reverted the mistake commit by creating a new commit for it, we actually didn't push it to GitHub. So, let's go ahead and do that:

```
git push origin master
```

Refresh GitHub to see the revert message near *index.html*.