The process of making a design responsive is complex and often requires a whole load of new styles for different size devices to wrangle a design into shape. When working on a responsive project, Sass has a number of useful features that can make our lives easier and make our code more maintainable.

In this video, we'll look at nested media queries in Sass, using variables in media queries, and creating a responsive mix-in to simplify your authored code. Media queries are one of the three pillars of responsive design. Fluid containers which are sized in percentages, flexible media, things like video and images that scale and don't breakout of their containers, and media queries.

We covered media queries in a previous A to Z CSS video. But in essence, they're a way to create conditional CSS that only renders when certain characteristics about the device that is viewing the content are true. So we've got an example here. We've got a box with a blue background and then a media query that says, when the width of the page is above 500 pixels, the background will be red.

Even in this very short example, there is some duplication which Sass can help us reduce. Using Sass, we can nest the media query declaration inside the braces of the box class. And that avoids having to redeclare the class a second time. Nesting can be a contentious issue among developers due to the way it can mask specificity issues.

But in this case, the nested media query doesn't add any additional specificity at all. And I personally find it a great way to make the code I write shorter and more readable as it group selectors and any related media queries together. When crafting responsive styles across a whole project, it's quite common to have a handful of major breakpoints.

Where number of separate media queries all handle the styles for broad categories of different size devices. These might be described as small, medium and large or thought of as the devices themselves, mobile, tablet, desktop. Whichever form of naming you prefer, it's likely that you'll need to reference the same breakpoint sizes a number of different times potentially across multiple different files.

And this is a perfect opportunity for using a variable. So let's have a look at an example. I got a simple page design here with a couple of media queries to handle the breakpoints between small and medium screens. The value of 500 pixels and 800 pixels have been used in a couple different places.

Now, I could have used any length unit here, could have used ems or rems or pixels. Pictures and pixels just for the sake of simplicity as the numbers are often a bit more relatable. We'll look at converting two relative units in a little bit later on in this video.

To make these pixel values even more meaningful and much easier to reuse, let's create a variable to reference each of our breakpoints. So I've got a media small for the 500 pixels and media medium for 800-pixel breakpoint. And I like to name my variables like this with a naming convention just to add a little bit of extra meaning.

But as with all variables, you can name these however you like. If you have your own preference, go ahead and use that. To use these variables, we might attempt to replace the pixel value in the media query just like we would with any other variables, just like in the example here where I've got background:$brand-color.

But this doesn't work and actually throws an error. Because the variable is being used within another string of characters for the media query declaration, we need to use Sass interpolation instead. Using interpolation, which you can learn more about in the previous episode, episode 9, I think, of this series, the variable expression is evaluated within the surrounding media query declaration.

To complete this example, we can replace all other instances of our pixel breakpoints with variables. This is an improvement on the raw CSS approach and we can now adjust the point at which our design responds to a small or medium screen just by adjusting the variable value. And this would then ripple out across of the different places that that's being used.

However, there's still a lot of duplication in a lot of the media queries themselves. Which we can address in the final section. To streamline the process of working with media queries and to reduce the amount of code that you have to type, just always a good thing It's possible to create a mixin to handle the outputting the media query itself.

So we can create a very flexible mixin, which allows us to create all sorts of different break points. We can create a mixin that responds to different properties and different values that we pass in. To do that I'll create a respond to mixin, that takes two arguments. One for the value of the break point, which would be something like 500 pixels, or 800 pixels.

And one for the CSS property that the media query should check, about the device, and therefore respond to. That might be the min-width property or the max-width property, it could even be a height based media query or aspect ratio based media query, some of that which is less common.

Calling the content block within the body of the media query means that the styles that we pass into the mixing block, We'll only have B output when the media query is true. So to use this mixing we use the include directive, we specify the mixing name and passing the two variable values.

For example. Respond to 600 pixels min-width, and then set the width property to 100% at that break point. If you find that you most commonly use min-width or max-width media queries, depending on whether you're working mobile first or desktop first. You could modify the mixin slightly and create a default value for the property argument.

By adding this default value, if the mixin is called without the second argument, the default one will be use instead. So using @include respond-to ( 600px ) Will actually create a min-width media query for 600 pixels and output the width. If we take a look at the compiled CSS, we'll see the resulting output.

We can take this mixin even further and convert any pixel based break points into Based or REM based values instead. If we use a pixels to Function. We can call that within the body of the mixin and then instead of outputting a pixel based media query, the result of our function expression will be added in place.

And we can ensure that we're using the relative units in all of our media queries going forward. When working with responsive design, there's always a lot to think about. So if Sass can help us reduce the amount of code we have to write, it can certainly help us speed up the process

