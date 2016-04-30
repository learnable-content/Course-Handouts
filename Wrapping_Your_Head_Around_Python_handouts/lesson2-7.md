![](headings/2.7.png)

# Advanced String Manipulation

Now we're going to do some advanced string manipulation. Particularly, we're going to see how to split strings and basically make better use of the data inside of a string. For that we will require these variables:

```py
fileContent = 'John Doe;\n350 5th Ave\n|\nJane Doe;\n100 7th Ave\n|\nJoe Daniels;\n11 1st Ave\n'

packages = {}
```

Semi colon is used to split customers and their address. Pipes split pairs of customers and addresses.

What we can do now is split the contents by `|` symbol:

```py
newStr = fileContent.split("|", 3)
print(newStr)
```

This 3 is basically limiting the number of splits. We have three items here, and that's why I've got this 3.

Now let's work with a `for` loop to go through the contents of the string and place the result inside the dictionary.

# Creating 'for' loop Definition

```py
for s in newStr:
    (a,b) = s.replace("\n", "").split(";", 1)
    print(a + " == " + b)
    packages[a] = b
```

First of all, remove newline special characters (by replacing them with strings of zero length). Then split by `;` only one time. The result should be assigned into the variables `a` and `b`. `(a,b)` is a **tuple** - we will look at them more detail a little later.

Next we simply take `a` as key and `b` as value and store them inside our dictionary.

Lastly just print out some information for testing purposes:

```py
print(packages)
print(packages.keys())
print(packages.values())
```