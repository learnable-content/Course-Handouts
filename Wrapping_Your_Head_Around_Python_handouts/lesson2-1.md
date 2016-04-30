![](headings/2.1.png)

# Variables and Strings

In this lesson, we're going to learn about **variables and strings**.

# Variables

So first thing I'm going to do is create a customer and for that I can just create a variable:

```py
customer = "John Doe"
```

When naming variables, you can use capital or lower case letters. Also you can separate letters with underscores or use mixed case, like `pickupLocation`.

Still, avoid starting variables with a number, or using special characters like the number sign, ampersand, percent, parenthesis, the pipe.

# Assigning Values to Variables

Let's say I want to have a pick up location:

```py
pickupLocation = "350 5th Ave"
```

Note I am typing the name of the variable without anything preceding it - there are no keywords.

Now combine variables:

```py
package = customer + pickupLocation
print(package)
```

`print` basically displays information in the console. If you run the script, you'll note that basically variables' contents was concatenated together without any kind of special formatting.

```py
package = customer + "@" + pickupLocation
print(package)
```

Now strings delimited with `@`.

# Creating Integers

Let's do some calculations:

```py
fare = 15
tip = 2
totalFare = fare + tip
print(totalFare)
```

We just sum up two numbers here.

# Formating

The output can be formatted:

```py
print(package + " with total of " + str(totalFare))
```

Note that using `str` we convert integer to string to be able to concatenate it - otherwise an error will be raised.

# Combining Integers with Strings

Now suppose we have an integer and a string that contains a number. We can sum them like this:

```py
fare + int("2")
```

`int` converts string to integer.