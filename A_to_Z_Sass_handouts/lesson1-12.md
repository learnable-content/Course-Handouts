CSS is a declarative language rather than a proper programming language. And many purists think that it should be kept that way. However, in my experience I've come across many times when having the power of logical flow control within my styling has been hugely beneficial. Fortunately, Sass can help us out here, as it has a number of features that bring the power of programming to CSS.

In this video we're gonna learn about the three different kinds of loops in Sass, working with conditional statements, and some practical applications for both of these powerful features. Let's start with loops. Loops are a programming construct that exists in many, if not all, proper programming languages. They come in a variety of different forms and are used to execute a block of code, or in the case of Sass, output a block of styles a number of times.

The way that the loop iterates depends on the type of loop being used. In Sass, there are three different kinds. We've got the @for loop, the @while loop, and the @each loop. Let's take a look at each of them in turn, no pun intended, and see how they work and what they can be used for.

First up is the @for loop, which is comprised of five different parts. We have the @for declaration to start loop, then we have a counter variable which is often written as i, short for iteration, and that keeps track of how many times the loop has run, how many times it's iterated.

The next thing we have is a starting value for this I counter. And then we have an ending value for the counter. And when the counter passes this end point, the loop will finish. We also have a keyword which is either the value of to or through, which determines whether the loop should run up to the end value.

I stopped before it reaches it, or run through the end value, which means running up to and including it. Finally, we then have the body of the loop which contains the styles that will be output. And these will probably use the value of the counter variable in some way, such as creating numbered class names or in some kind of calculation.

So in this example, we've got a loop that runs from one up until including ten. And it's gonna output a series of box classes. The first time will be box one, than box two, than box three, all the way up to ten. And each one of them will have a different width, where we're multiplying ten pixels by whatever the current value of our iteration counter is.

So we will end up with ten different box classes standing at ten pixels width, going all the way up to a 100 pixels width. These loops are really useful when creating custom grid systems with numbered class names for different columns with various widths. The Sass while loop is slightly different and slightly more powerful.

Instead of having a counter that increments by one each time, we can control how the counter changes manually. @while loops take the following form and they're comprised of four key parts. We have the starting value of the variable, again here we're gonna use the i variable, and give it an initial value of 10.

We then have a Sass script expression, which forms a condition for the loop, which must evaluate to True in order for loop to keep going. In this case, for the style block to be output, i must be greater than zero. As before, the body of the loop contains our block of styles, and we use counter variable or our condition in some way.

And then the last part is a modification to the condition. Here we're decreasing the value of i by 2. So this is where the @while loop is a bit more powerful because instead of just counting up and increasing by one every time we can control what is done to our counter variable.

So this loop outputs some very similar code to that of our @for loop, but in this case the numbered classes are only even numbers that count down from ten to two. Personally I attend to use the @while loop a little bit less often than the @for loop, but it's useful to have that option of having tighter control of how the loop actually iterates.

The final loop available in Sass is the @each loop. The @each loop is used to iterate over a collection. That means a list variable or a map variable. We're gonna look at map variables in a lot more detail in the next episode. A Sass @each loop will take the following form.

We start off with a collection, in this case, a list of names, then for each item in the list, the loop will iterate and store the value of the current item in the name variable. In the body of the loop this name variable is then used to create a dynamic class name and output an image with a specific file name for each member of the team.

Each loops are really useful when dealing with lists of things and wanting to do something specific for each item in the list. We'll look at another example of this little bit later on in this video. But first let's take a look at another way of controlling how our styles are output.

Another concept that exists in most programming languages is conditional statements. These will only output certain lines of code if a predefined condition evaluates to true. In the case of Sass, the condition is a Sass script expression which should evaluate to either true or false. In this example the display block styles will only be output if the variable is visible is set to true.

Sometimes we wanna output one set of styles if the condition is true but other styles in all other cases. Taking the example of visibility a little bit further, we could add a second part to the condition to say if it's visible, set display block, else set display none.

In this case only one line of CSS is ever output. Think of it a bit like a fork in the road. Each time you approach the fork you have to choose to go one way or the other. Finally, it's possible to set up multiple conditions, with if and else if, although sometimes this can get a little bit long and complex.

But here is an example which sets a series of elements widths based on a range of variable values. So we're saying, if the width is small, set width 25%, else if the width is medium, width should be 50%. Else if the width is large, the width should be 75%, but in all of the cases, the width should be auto.

As with the previous examples of conditional statements we've seen, only one of these widths will ever be output. Conditional statement are really powerful way to control the styles that get output under different circumstances. And while they may be a little bit foreign to CSS and to styling things they can be incredibly useful when building out complex components or perhaps when building out your own mini frameworks.

So let's wrap up with a practical example. A few years ago, I was tasked with building a live style guide for a project I was working on. And one of the features of the style guide was to show all the colors used in the project along with its Sass variable name and a text code.

We'll look at a simplified version of this, here in this video. And then in a future video, I'll show you how this can be refactored and made a little bit more compact. So here I've got some static CSS that sets up the styling for a series of boxes for some color swatches.

The layout is handled with a bit of flex box to enable easy horizontal and vertical centering of all the text inputs inside each box. If you wanna dive into Flexbox in a bit more detail, we have a mini-course here on SitePoint all about Flexbox fundamentals. So here each box or each swatch is gonna have a different background color and show the variable name and the corresponding hex code inside.

Let's first set up a series of variables and create two lists, one for the variable names and one for the list of colors. So our names will be white, red, green, blue, and black. And here are our colors. I won't read out the hex codes, but you'll be able to see them show up in just a second.

We now need to iterate through each name in the list and create a modifier class for each of the colors and output its name. To add the color, we need a way to reference the colors variable from within the loop. To do this we can create a counter variable, i, and then use the Sass nth function which will return the nth item in a list.

After we've used the nth function we store it in a variable so that it can be used as both the background color and as the content property which will display the hex code to the user. Everything is looking pretty good but we can't read the text in the black box cuz we've got black text on a black background.

A quick and dirty solution to this would be to check the lightness component of the color, and if it's less than 50% we could set the text color to white. And we can do that using a conditional statement. For more complex of loops and conditional statements and to improve on this quick and dirty method of switching the text color for reability, we could create a function that measures actual color contrast instead of just measuring lightness.

This is a little bit advanced, but I found a great example of a function like this by F stop, over on GitHub. Which you could check out if you needed a slightly more advanced functionality. CSS may be a declarative language, but adding these programming features for loops and conditionals make Sass an incredibly versatile and powerful extension to the language.

