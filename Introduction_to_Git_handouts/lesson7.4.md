![](headers/Git Lesson 7.4.jpg)

# Introduction

In the terminal check out to the `featureB` branch with

```
git checkout featureB
```

You want see changes that were made on the `featureA` branch, which makes sense because we've checked out into `featureB`.

# Pushing to Branch featureB

Once again replace `h2` with

```html
<h2 class="intro-text text-center">Feature B Branch<strong>Our second branch!</strong></h2>
```

Add the file changes with

```
git add .
```

and then commit with

```
git commit -m "Initial commit on feature B"
```

Lastly, push our entire branch over to GitHub with

```
git push origin featureB
```

The new branch should appear on GitHub.