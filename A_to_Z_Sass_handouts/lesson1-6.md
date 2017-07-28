**Functions** are a core concept in many programming languages. But creating and using our own custom functions isn't something we can do in normal CSS. However, Sass brings the power of programming to the table and it does allow us to create our own custom functions for performing all sort of different common everyday tasks.

In this episode, you'll learn what functions can do and why they are useful. How to create and use your own custom functions in Sass and examples of functions in the real world. Functions wrap up a named sequence of instructions that generate a value. They often accept input parameters called arguments and they return back an output value.

Functions provide a blueprint for a repeatable process that takes one value or sometimes multiple values, and performs some kind of calculation on them, and then sends back a new value, which we call the return. Their idea for performing mathematical operations or converting one type of value into another type of value.

Using functions hands over all the responsibility and all of the mental overhead of doing complex calculations to a machine, to a computer, rolls on leaving all that work up to ourselves. So this can help us work faster and reduce the risk of human error which is very much a common thing when working with Sass.

If you are not familiar with programming then concept of functions can be a little bit abstract to begin with and can be tricky to get your head around, so let's take a look at an example. A common web development task is to take a value that is in pixels and convert it into a relative unit, like rems, or ems.

When working on a responsive project especially, it's often preferable to use relative units like rems instead of pixels so that we can build kind of like of a flexible system of proportions rather than sizing every last component to absolute pixel values for things like the width or the height or in spacing values.

This allows the shape and size of elements and the spacing around them to kind of expand and contract as we change values like the font size. While using rem values produces more flexible elements, it's sometimes easier to visualize pixel values and sometimes it's easier to think in a certain number of pixels rather than some arbitrary decimal value of rems or ems.

So we could create a Sass function that converts pixels into rems and it would give us the best of both worlds. We'd be able to think in pixels, but yet, still have all the benefits of working with rems. We wouldn't constantly need to be reaching for the calculator.

I hate CSS maths so if I can get a machine to do all this for me, then so much the better. Before we look at the Sass syntax for creating and using a function, let's first just double check that we're happy with the calculation itself that would convert a pixel value into a rem value.

So the calculation for converting a pixel value into a rem value is to divide the pixel value by 16, by the base font size. And then we multiply that by 1rem. So we can create a Sass function that can automate this process for us, and that would look as follows.

So we define the function with the @ function directive. And I've given it the name px-to-rem for pixels to rems. And it is gonna accept one input parameter which I've called value. Then, we're going to perform a calculation by dividing the value that was passed in by the base font size and multiply it by one rem, and then we'll return that value back out of the function.

To use the function, we just call it by it's name and supply the input value inside parenthesis. This will convert 20 pixels to 1.25 rems and the return value will Will be output in the CSS. So instead of reaching for a calculator or doing a quick mental sum in our heads we can leverage the power of Sass to do that for us.

And now, we can focus on solving much more interesting problems. In the previous example, we demonstrated the essence of functions taking, One value and turning it into something else, turning into another value. But in the real world we might want to, we might need to, make our functions a bit more flexible so they can accept different types of input.

So we gonna make our function more flexible by allowing it to accept either a pixel length or a number value which is gonna be assumed to be a number of pixels, and we gonna convert that into rems. So to do that, I'm gonna make another function, which is gonna turn any length value into the same number but without the units.

And once we've done that we can combine the two functions together, so to create a function that's strips the units from a length value, we need to divide that length by a single unit of itself. So if we wanted to convert 20 pixels into the number 20, we would divide 20 pixels by 1 pixel.

If we had ems instead, if we wanted to convert 80 ems into the number 80, We would divide 80ems by 1em. So we can create a function that does exactly that. Here, I've called it strip-untis, it takes in a length value and it returns a number, the same number as the length but without the units.

Having created this strip-units function, we can now update our px to rem function to strip out any of the units from the input value and from the base font size. So, having done that inside the body of the px rem function, we're only if it could be working with numbers rather than lengths.

So, now we can call this function with either a pixel length or a number as the input values. And this will compile to font size 1.25 rem and padding 0.9375 rem. So not only is our function flexible but it's really really useful. Instead of seeing values like 0.9375 rems in the start sheet trying to work out where that might have come from, we can see the number 15 and almost immediately get a sense of a kind of length or a kind of amount of padding in this case that we are talking about.

