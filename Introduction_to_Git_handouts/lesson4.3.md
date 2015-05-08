![](headers/Git Lesson 4.3.jpg)

# Introduction

Let's practice with pushing again.

# Making changes & pushing to Git

Open *index.html* and scroll down to after the carousel between lines 109 and 116. Instead of "Business Casual" type in

```html
<h1 class="brand-name">This Git Course</h1>
```

Also change "Start Bootstrap"

```html
<strong>Kauress</strong>
```

Run 

```
git status
```

You will see that *index.html* has been changed but isn't yet staged.

```
git add index.html
```

to stage the file.

Commit our stagged file with

```
git commit -m "Changed items after carousel"
```

Push these changes to GitHub:

```
git push origin master
```

Go to your GitHub repo and refresh the page. Clicking on the commit message near the *index.html* will show you the deletions in red and additions in green.

You can also see your changes side-by-side by clicking on Split.

Come back to terminal and now let's view a history of our commits till now:

```
git log
```

This command records all the commits with specific reference numbers, authors, dates, and commit messages.

To see all your commits on one line, which is useful if you have a lot of them, type in

```
git log --pretty=oneline
```

Press the `Q` key to exit.

Now you have a sense of why Git is a version control tool: all it's really doing is tracking changes to your files.