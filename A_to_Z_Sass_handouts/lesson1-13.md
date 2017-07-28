In a previous video, we discussed the various data types of Sass variables. One variable type we didn't have a huge amount of time to go into detail on is map variables, but the time has come to fix that. So in this video we're gonna learn all about map variables, how to create them and what to store in them.

We're gonna look at using values from mapped variables, querying and merging maps together. And finally look at a practical example of using maps in a real world project. Map variables are a store of key and value pairs. They're a feature of Sass 3.3 and above. And are probably one of the biggest game changers that Sass ever seen.

They're similar to list variables, but each item in a map also has a unique key or a unique label. A Sass map looks very similar to a JavaScript object or like the key value pairs in a CSS style block. The series of key-value pairs are separated by commas instead of semicolons.

And the whole thing is wrapped up in a pair of parentheses to group all of the items within the map together. Map variables can be used to store any valid Sass data type and you can even have a map of maps. I'll just paste one in here so you can check it out without having to watch me type it all.

This is a great example of storing a whole series of different settings together in a single variable with a map for colors, a map for font families, and a map for font sizes. Storing information in these more complex data structures means that we need a new set of tools for accessing these values from within the map.

So let's take a look at some of those. We will work with an example of just a single map rather than maps within maps. And we'll take a classic example of having a map of font sizes that you might be used to set up some sensible defaults for the headings and the body copy of a project.

So to access a value in the map, we refer to it by its key which is the first bit before the colon in the map. So in our font sizes map h1, h2, h3, h4 and p are all keys of the map. So to get the value of 50 pixels from within the font sizes map, we use the map-get function.

And that takes two arguments. First, the map and the second one is the key that we wanna access. If we had a whole series of different values that we wanted to get out of the map, we could perhaps combine this with an each loop, like we saw in the previous video.

In this case, Sass knows that we're iterating over the map. And we don't need to use the map-get function. So, if we create an each loop, we're gonna get access to the selector and the font-size in each of the elements of the font sizes map. We'll create the selector and then out put the font-size.

When building complex components or creating library code, it may be necessary to check that a map contains a particular key before trying to get the value out or manipulating it in some way. If you try to use a key that isn't found, Sass will throw an error. And sometimes you need to prevent that from happening or have it fail more gracefully.

So, for this purpose, Sass has a map-has-key function which returns true if the key exists, and returns false if it does not. So this can be combined with a conditional statement like so. So our settings map has two keys, one for media queries and one for enlarge-text. And if we wanted to check that enlarge-text key exists before doing something with it, we would rewrite our conditional statement using map-has-key and use it if that key exists.

Otherwise, set the font-size to 100%. Another feature of maps is the ability to merge two maps into one, or to add new keys into an existing map. Personally, I've not found a huge amount of need to do this on many occasions, but I'll include it here just for the sake of completeness.

Imagine we've got a button mixin which has got some default settings for things like color, background, padding and the amount of border radius. We can make this mixin more flexible by letting it accept an optional map of additional options to change how it looks. And then merge our options and settings together before outputting the series of properties and values.

Not only does this let us extend our button, it means we can override any of the default settings with our own custom options. This is because a map can only have a unique set of keys. If both the settings and the options maps contain the key color, then the second color would override the first.

Dealing with complex structures like maps can seem a little bit abstract outside the context of real world examples, so let's fix that too. If you watched the previous episode about loops and flow control, you might remember we looked at an example of creating a series of color swatches for a style guide.

At the end of that video, this is the code that we were left with. The crux of the exercise was to take two list variables, one for color names and one for hex values, to output dynamic swatches of colors that are used within this hypothetical project. We can improve on this by instead of having two separate lists, we can combine those two lists into a single map variable which will greatly clean up the code.

Not just in terms of the variable itself but in terms of how we use the loop as well. So we'll create a map variable called colors where each key is the color name and each value is the hex code. Now we need to update the loop to pull out the name and the color for each item in the map.

We do that as follows, instead of just creating a single variable for each element in the list, we create two, one for the key and one for the value. So, each time the loop goes round, we'll have access to the name, which is the key, and the color, which is the value in the colors map.

So here we've combined two variables into one and removed the need to fetch values from a list based on their nth index. All in all, this is a much neater solution and one that's much easier to maintain.

