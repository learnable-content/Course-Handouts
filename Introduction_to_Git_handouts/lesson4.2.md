![](headers/Git Lesson 4.2.jpg)

# Introduction

In the previous section we sent the contents of our *theme* folder to a remote repo on GitHub. We did this without making any changes to any of our code files. In this section we'll edit our *index.html* file, then take a snapshot of our change, and send it off to the remote repo on GitHub.

# Making changes & pushing to Git

Make the following changes in the *index.html*:

```html
<title>Git</title>

<div class="brand">Git</div>

<div class="address-bar">Learning Git</div>

<a class="navbar-brand" href="index.html">Git</a>

<a href="index.html">Add</a>

<a href="about.html">Push</a>

<a href="blog.html">Commit</a>

<a href="contact.html">Status</a>
```

Let's send the modified version of our *index.html* file to GitHub.

Type in

```
git status
```

This shows you that *index.html* has been modified, but it hasn't yet been staged or committed.

Add it to the staging area

```
git add index.html
```

You could just use the `.` instead of `index.html` (this is useful when there are many files to add to the staging area).

Run

```
git status
```

This lets us know that we added *index.html* to the staging area and it's ready to be committed.

```
git commit -m "Changed title, subtitle, and navbar items"
```

We committed on the master branch, which is our main branch; the commit has a specific reference number. Additionally, there is also a commit message with the number of additions and deletions to *index.html*.

Push our work to GitHub

```
git push origin master
```

This pushes our file changes from the master branch of our local repo to the remote repo on GitHub.

Go ahead and refresh GitHub page. Here near *index.html* you can view the commit message - click on it. The minus sign in red denotes deletions in the file, and the addition sign in green denotes things that you added to your *index.html* file. The blue addition sign is for adding comments, o if you were working in a team, your team members could add comments to the additions and deletions in your commits.