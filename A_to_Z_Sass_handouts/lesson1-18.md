In this series, we've looked at all the fundamentals, powerful features of Sass from variables and nesting to functions and flow control. Further to these features, Sass has a whole load of of really useful functions and utilities which turns CSS from a purely declarative language into something more like a scripting language.

In this short video we're gonna look at one such feature and some practical applications. Today we're gonna look at the Sass random function. Many programming languages have the ability to generate random numbers. These are useful for building games, generating dummy data or creating algorithms. Sass is slightly special because even though it can generate a random number at compile time this number will remain constant, until the styles are recompiled again.

To illustrate this, let's take a look at using the random function in a simple example. I've got a box here with a minimum width and a height so that we can see something on the rendered page. Over to the left hand side. Using random let's generate some random dimensions for the box.

The random function takes a single argument for the upper limit of the random number to be generated. When using this function the lower limit is always 1, but the way we've used it here, by passing 500 into the function we'll generate a random number between 1 and 500.

If we save this code and compile we'll see the randomly generated dimensions for the box. If I refresh the page the dimensions remain exactly the same. This is because the random number is only generated at compile time. If I forced the code to recompile by saving, the two new numbers are generated and the box dimensions change once more.

This function is simple to use, but how likely is it that you'll ever need to generate a random number in CSS? In the past, I've used this for generating random colors for a grid of boxes when prototyping an image grid. So instead of searching for or creating a whole bunch of different images whilst in development mode, I used Sass to generate a whole load of different colored images, or colored boxes.

So we can combine a for loop with rgb backgrounds, each with a random number from 1 to 255, and this will provide some pretty interesting effects, so here we've got a for loop with a counter variable i which will iterate from 1 through to 100. And we're gonna create a series of boxes and each one of those boxes will be styled differently.

We're using nth-child and passing in the iteration counter into that. So the first time it will be box nth-child 1 then box nth-child 2, box nth-child 3 all the way up to 100 and then we're setting the background color. Using the rgb function to generate three random values between 1 and 255 for each of the components of red, green, and blue.

Another potential use case that I discovered recently is creating particle effects. There was an amazing article on CSS-Tricks. About combining sass and random number generation, and animation, to create some really amazing effects. Highly recommend checking it out. This uses the random function to randomize the starting position of a series of little, tiny particles and then animating them.

Each with a random animation duration and animation delay to create a really impressive effect. And while this is not something that would have a place in every single project, it's always great to find these little gems hidden inside of libraries like Sass. That might some time, just one day, come in useful.

