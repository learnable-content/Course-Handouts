![](headers/Git Lesson 7.5.jpg)

# Introduction

In this step we will talk more on pulling and pushing. Let's again assume that we're working with Laura, our imaginary teammate who's making changes to the `featureA` branch along with you.

# Pulling, pushing and resolving conflict on feature A

Head over to GitHub to the `featureA` branch, and open up the *index.html* file. Scroll down to the intro text, `.text-center` element and delete all the `p` tags, including the text inside. Instead type in

```html
<p> Basic Display Features For Customers </p>
```

Commit the change with a message "Changed text Lara".

Head over to your terminal and type

```
git status
```

Everything is okay, so let's check out to the `featureA` with

```
git checkout featureA
```

Make some local changes: delete the `p` tags from the same section of *index.html* and type

```html
<p> Basic Features For Customers </p>
```

Now in the terminal:

```
git add index.html
git commit -m "Edited paragraph"
```

As you previously learned it's good practice to update your local branch with the latest commit from the remote:

```
git pull origin featureA
```

We have a merge conflict. Open up the *index.html* file. Let's assume that we discussed what change we want to keep with our teammate Lara. We've decided to keep our change and incorporate Lara's change as well, so type in

```html
<p> Basic Display Features For Customers </p>
```

Tidy up the conflict area. Once you're done, go ahead and save the file.

Now in the terminal

```
git add index.html
git commit -m "Incorporated changes"
git push origin featureA
```

The changes are now pushed to GitHub.