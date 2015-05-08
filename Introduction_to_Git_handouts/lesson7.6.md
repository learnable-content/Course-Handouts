![](headers/Git Lesson 7.6.jpg)

# Pulling into Branch featureB

So far, we've been working on the `featureA` branch. In your terminal checkout into `featureB` with

```
git checkout featureB
```

Then go to your code editor and scroll down to the `.text-center` element where it says "Feature B branch". Delete the `p` tags and the text inside and type

```html
<p>Premium Display Features For Customers</p>
```

Now, come back to the terminal

```
git add index.html
git commit -m "Edited paragraph on feature B"
```

Let's do a pull and see what's going on Lara's side before we push our work:

```
git pull origin featureB
```

It says that the branch is up-to-date, andt his is because no new changes have taken place on the `featureB` branch on the remote repo. Push your work to the remote:

```
git push origin featureB
```