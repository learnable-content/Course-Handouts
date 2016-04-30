![](headings/2.2.png)

# 'if' conditional

Now we're going to look at how **conditional flow** works in Python . Start with `if` condition:

```py
customer = "John Doe"
pickupLocation = "350 5th Ave"
package1 = customer + pickupLocation

if "350 5th Ave" in package1:
	print("Customer Found")
```

We check if `package1` is equal to a particular address and peinr "Customer found" if it does. Note the `:` after the condition and the indent before the `print`.

Now suppose we have many customers and pickup locations and wish to compare them. In this case you may use `elif`:

```py
customer2 = "Jane Doe"
pickupLocation2 = "100 7th Ave"
package2 = customer2 + pickupLocation2

customer3 = "Joe Danields"
pickupLocation3 = "11 1st Ave"
package = customer3 + pickupLocation3

if "350 5th Ave" in package:
    print("Customer 1 Found")
elif "100 7th Ave" in package:
    print("Customer 2 Found")
else:
    print("Customer 3 Found")
```

So if the first condition is true, "Customer 1 Found" is printed and other conditions are not checked. If the first condition is not true, the second one is being checked and if it false again, "Customer 3 Found" is printed out.

`elif` means "else if".

# Comparisons

Now let's work with integers and compare them:

```py
streetNumber = 1

if streetNumber >= 0 and streetNumber < 200:
    print("Customer found in 100 to 200 block")
elif streetNumber >= 200 and streetNumber < 300:
    print("Customer found in 200 block")
elif streetNumber >= 300 and streetNumber < 400:
    print("Customer found in 300 block")
else: 
    print("Customer found in 400 and above block")
```

`>=` means "greater than or equal to", `<` means "smaller than". `and` is a special logical operator, so the first condition is true only if street number is greater than or equal to zero **and** less than 200.

Note that we also have multiple `elif`s.