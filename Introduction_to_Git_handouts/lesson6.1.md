![](headers/Git Lesson 6.1.jpg)

# Introduction

So far our work flow has been one-way: we've sent changes from a local repository in our *theme* folder to the remote repo on GitHub. In this lesson, we'll reverse the workflow: we'll get changes from our remote repo into the local *theme* folder.

For this lesson I want you to imagine that you're working with a teammate who has access to the same repository on GitHub as you. Both you and your teammate will be adding, committing and pushing file changes over to GitHub. However, since we actually don't have a teammate, we'll have to make changes on their behalf. We'll do this by editing files on GitHub itself. This will act as a proxy for your teammate who hypothetically would be pushing over their changes to GitHub.

# Fetching & Merging Changes

So, go over to GitHub and open "readme.md". Click on the pencil icon in the top right to edit the file. Remember, we're making changes on behalf of a teammate, so if you had a teammate, he or she would be editing *readme.md* locally and then pushing over their changes to GitHub.

Delete everything in and type in "1st edit by Lara". Next, come down to the bottom of the page and type in a commit message "1st edit by Lara". Then press the green Commit button.

Open up *readme.md* file in your *theme* folder. As you can see, it doesn't correspond to the *readme* in your remote repo which has new changes. Let's update our local *readme* file with these new changes. In your terminal run

```
git status
```

This lets us know that our working directory is clean.

In order to incorporate changes from the remote repo into the local repo, we will use two git commands:

```
git fetch
```

And this is pretty self-explanatory: Git will fetch changes from the remote repo. Refreshing the *readme* file, we see that the new changes haven't been incorporated. This is because even though we fetched changes, we haven't merged them.

```
git merge origin master
```

This shows us that a fast-forward merge was performed. Don't worry about what fast-forward means, we'll come to it later. The plus and minus signs show you the proportions of additions and deletions to *readme.md*.

Refresh your local copy of *readme*. You should see the new changes.

Let's practice this once more. Go to GitHub, open the *readme.md* file for editing and add another line "2nd edit by Lara". Scroll down and write the commit message "2nd edit by Lara". Then press the green Commit button.

Repeat the fetch and merge process again to incorporate remote changes:

```
git fetch
git merge origin master
```