Sass brings a lot more power to CSS and starts to make it feel like a real programming language rather than just a series of property and value declarations. One key feature that enables this programmatic field is **Sass variables** which can hold a number of different types of data.

In this episode, you'll learn the seven core data types in Sass, and how we can manipulate and operate on these various values. Sass variables can store a number of different data types, including numbers, strings, colors, booleans, nulls, lists and maps. These different data types allows to create variables for all sorts of different CSS values.

A variable is just a handy label for some arbitrary value, and they can help make our code easier to read and quicker to update. Let's look at each of these different data types in turn to clarify what they are, how to use them and the kinds of values that we can put inside each of them.

So, let's start with **numbers** that are used a lot in CSS from setting margins and font sizes to border radius and line height. Numbers come in a few different flavors including integers, which are whole numbers and floating points, which are decimals, and length values, like 10 pixels, 20 ems, or 50%.

**String** variables stole strings of text and they're found in a number of CSS values including font families, colors, or URLs. Strings in CSS are found both with and without surrounding quotation marks, and they can be said to be either quoted or unquoted strings. Sass just like regular CSS doesn't differentiate between strings with or without quotes. The only exception is when dealing with some specific CSS values like sans serif or inherit which shouldn't be quoted. In Sass, color names also have special meaning so they should always be unquoted. But in all other cases strings should be quoted and I favour single quotes because they are easy to type.

**Colors** come in many forms such as named colors, hex codes, rgb and rgba or hsl and hsla. Colors are their own data type because they can be manipulated by color functions which we looked at in the previous episode. They can be added and subtracted from each other to produce new colors, it's not something I do very often but it is possible with Sass.

**Booleans** are either true or false, and they aren't particularly useful for setting values for CSS properties. But they are very useful when combined with logical flow control whilst building complex components, or building frameworks or library code.

**Null** is a special data type which represents something that could be said to be an empty value, again, their use isn't that common but one good example is. If a variable contains a null value, then applying this to a CSS property will cause that line of code to be removed at the compile time.

**List** variables contain multiple values, and they're either separated by a comma or by a space. They can be used to represent shorthand declarations for things like marginal padding or for font stacks. You can have a list that contains other variables or even a list of lists.

Also there is **map** variables. These contain a store of key and value pairs like JavaScript objects or like a Ruby hash, and they're a very powerful new feature from Sass 3.3 onwards. There's a lot to discuss with these Map variables so we'll cover them in more detail later

So with all these different types of variables, what can we do with them? With whole numbers or decimals, we can add, subtract, multiply, divide or modulo which returns the remainder after a division. When using mathematical operations with length values in SaaS, these are values with units at the end like 10 pixels over 20 ems. We do need to be mindful of the length units as many of them are incompatible.

Lengths with matching units can be added or subtracted from each other. However lengths, even with matching units, can't be multiplied together. Dividing lengths with the same units is gonna result in a number with no units just like it would in regular mathematics. This can be a handy trick for stripping the units from any length value.

So you can perform other Sass operations on a plain number value instead of having to deal with the length. If you do need to perform calculations with mixed units this can actually be done in normal css with the `calc` function, and this is supported in IE9 and above. 
