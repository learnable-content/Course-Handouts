![](headers/4-7.jpg)
# Code Refactoring

In this step we will refactor and clean up our code.

With Less you can keep the code DRY by writing less code and by not repeating yourself. However in the `bottom` section we're using multiple times the class `inline` with the namespace `inline_list`. That's too much, and this is against the principle of writing less code.

First of all, remove all styling for the `inline` class from the `bottom`. Next define the following rule:

```less
#bottom {
 	div {
 	 	.inline {
 	  		#inline_list;
 	 	}
 	}
}
```

This way we are reducing the amount of code duplication.

Now the `h3`:

```less
#bottom {
 	h3 {
		padding-bottom: @padding;
	 	.bordered(xxx, xxx, @light, xxx);
	}
}
```

So now we have polished the design and also refactored and cleaned up the code.