![](headings/2.4.png)

# 'while' Loops in Python

Now we're going to look at `while` loops in Python.

Again we have three different customers:

```py
customer1 = "John Doe"
pickupLocation1 = "350 5th Ave"
package1 = customer1 + pickupLocation1

customer2 = "Jane Doe"
pickupLocation2 = "100 7th Ave"
package2 = customer2 + pickupLocation2

customer3 = "Joe Danields"
pickupLocation3 = "11 1st Ave"
package3 = customer3 + pickupLocation3
```

Add three packages:

```py
packages = [package1, package2, package3]
```

Now add an index. Remember that lists are indexed starting from 0.

```py
index = 0
```

What we will do now is traverse the list using `while` loop:

```py
while (index < len(packages)):
    print(packages[index])
    index = index + 1
```

So we traverse the array while the `index` is smaller than length of `packages` list. Note that index has to be incremented by one after each cycle.

# Working with Strings

Now let's do something when the cycle ends - for example, print a message:

```py
while (index < len(packages)):
    print(packages[index])
    index = index + 1
else:
    print("no customers to print. index=" + str(index))
```

Remember we have to use `str` to transform integer into string, otherwise an error will be raised.