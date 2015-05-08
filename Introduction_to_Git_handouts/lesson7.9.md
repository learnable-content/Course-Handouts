![](headers/Git Lesson 7.9.jpg)

# Introduction

In this section we'll do a no fast-forward merge by merging our `featureC` branch into the `master` branch.

# Using No Fast forward merge

In the terminal checkout into the `featureC` branch with

```
git checkout featureC
```

Open up your code editor and change the color and size of the `footer` text:

```css
#footertext {font-size: 22px;}
```

```html
<div class="col-lg-12 text-center" id="footertext">
	<p "style=color:#fab11c">Git 2015</p>
</div>
```

Go back to the terminal and add these files to the staging area with

```
git add .
```

This is one of those cases where adding all files comes in handy rather than typing the file names one by one.

Commit our changes with

```
git commit -m "Changed footer text color and font size"
```

Now checkout into `master`

```
git checkout master
```

and let's perform a no fast-forward merge. Unlike the fast-forward merge where the HEAD simply points to the latest commit on the branch with the most recent change or most recent commit, with this type of merge a separate merge commit will be generated.

```
git merge --no-ff featureC
```

You will be asked to write merge commit message. Write anything and then exit the editor.

Now do

```
git log --pretty=oneline
```

You will see your merge commit.