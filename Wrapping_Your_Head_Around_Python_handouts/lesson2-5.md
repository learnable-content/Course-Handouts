![](headings/2.5.png)

# 'for' Loops

Now, we're going to learn about `for` loops. Here is the sample data for our program:

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

packages = [package1, package2, package3]
packages2 = {customer1:pickupLocation1,customer2:pickupLocation2,customer3:pickupLocation3}
```

First of all, let's loop through the list of `packages` using `for` loop:

```py
for p in packages:
    print(p)
```

So `p` is a local variable that takes value of each package in cycle.

# Making a Set of Items

To traverse a dictionary you need to provide a set of items:

```py
for k,v in packages2.items():
    print(k + " address=" + v)
```

Note than now we have two local variables: `k` will store a key and `v` will store a value. Using `items()` we fetch items from the dictionary.

Instead of traversing pairs of keys and values, you can fetch only keys or values using these functions:

```py
for k in packages2.keys():
    print(k)
    
for v in packages2.values():
    print(v)
```