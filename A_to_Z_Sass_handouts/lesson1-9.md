We've discussed variables and their various data types. Variables can be used to set all sort of values for all sorts of CSS properties. But if a project calls for a variable to be used as a selector name or a property name, we need interpolation to make everything work properly.

In this video, you'll learn what interpolation means. The difference between string concatenation and interpolation, using variables in selectors and property names. And using variables in media queries for responsive design. Let's start off with a bit of definition. Interpolation is a term often used in mathematics to refer to the practice of constructing new datapoints within the range of an existing set of known datapoints.

But that still sounds a bit complicated to me. So how about this, interpolation inserts something into something else. In the Sass world, this usually means inserting a Sass expression, such as a variable, a function call or a mathematical calculation into another string, another selector, or another property name.

Sass uses a special syntax for inserting values into other values that take the form of a hash sign with two curly braces, and then the expression goes on the inside of the braces. This syntax is also found in the Ruby programming language, and that's where Sass has its roots.

Let's take the following example, where I've got a variable called image that holds the value logo.png. I've got a selector for the logo, and I want to apply the image as a background image. If I was to write everything out manually, the image URL would look as follows,where we have images/logo.png.

But instead of writing it out manually, I'm going to use the variable. If I add the variable name within the URL string, Sass doesn't throw an error but the image doesn't show up. Adding image within the quotes for the path creates a literal string images/$image as the URL, which isn't right.

It isn't point to our image file. If we want image to be used as a Sass variable, we have two options. Firstly, we could use something called string concatenation, which is the process of joining two strings together using a + sign called the + operator. Here we add the string logo.png from the variable onto the end of the images/string in the URL.

The second approach is to use interpolation and insert the value of the variable within the URL string. To do that, we can rewrite the code as follows. Within the interpolation braces, the Sass expression is interpreted first, and then inserted within the string. When using interpolation, any Sass expressions such as a function core, or mathematical calculation can be performed.

And then the result of that expression will be inserted in its place. You might ask why there are two different approaches for doing almost exactly the same thing. Well, interpolation can be used for inserting values into more than just strings. We've just seen two approaches for inserting a variable into a string.

But now let's take a look at working with selectors and property names instead. In the following example, I've got three variables. One's called selector, one's called property, and one's called value. Now these could have been named absolutely anything, but I've tried to give them a name to illustrate where they're gonna be used, just for the case of this example.

So we can use the value variable in the typical way to set the color property. When the Sass compiles the variable name is substituted for the variable value, which in this case is red. If we want to use the selector variable in the selector itself, we need to use interpolation as string concatenation with the + operator doesn't work.

And this is because + is actually used as an adjacent sibling selector. So instead we use interpolation to create the selector p.highlight in the compiled CSS. We can do a very similar thing to work with a variable within a property name as well. Interpolation is a very useful feature.

Even if variables in selectors or properties aren't as common as using variables for values, it's really great to know that this tool is there when we do need it. One final area where interpolation comes in very useful is when working with media queries. Using variables and media queries is worth looking at because, it can be a bit confusing to know when interpolation is or isn't needed.

So let's take the following example of a breakpoint variable, which is set to a number of pixels. This breakpoint variable can be included in a media query as the value part of a min-width or a max-width media query. Sass has no problem with this at all, and it all works perfectly.

But imagine if we use these min-width media queries quite a lot and with this particular value, we might get a bit tired of typing out the whole thing of screen and min-width breakpoint all the time. So instead, we could create another variable for the whole query itself, and maybe even interpolation to insert the value of breakpoint.

But if we're not to use this query variable for the media query, Sass will throw an error. So there's a very simple workaround for this. And instead of just using the query variable by itself, we can use interpolation and everything works as planned.

