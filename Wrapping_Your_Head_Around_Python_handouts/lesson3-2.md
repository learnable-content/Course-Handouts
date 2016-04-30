![](headings/3.2.png)

# Introduction

Now we're going to look at **lambdas**. We've seen a little bit of how this works. I'm going to create a familiar function that we used earlier:

```py
def calculateFee(miles):
    result = miles * .5 + 2.50
    return result
    
print (calculateFee(10))
```

# Simple Example of a Lambda

Here is a small example of a lambda that we've already seen:

```py
add = lambda n1, n2: n1 + n2
print(add(1,3))
```

And here is how our initial function may look like as lambda:

```py
calculateFee2 = lambda miles: miles * .5 + 2.5
print(calculateFee2(10))
```

# Lambda within the Function

What's more, lambda can be placed directly into function's body:

```py
def calculateFee3(miles):
    resultTemplate = lambda miles: miles * .5 + 2.5
    return resultTemplate(miles)
    
print(calculateFee3(10))
```

What happens here, is you take a number of miles and then pass it to the lambda which calculates the value and returns it as a result.