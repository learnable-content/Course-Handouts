In a previous video about creating custom functions in Sass, we created a function that converted pixel values to rem values by manipulating their units. We can create our own functions for all sorts of different applications in Sass. But there are also a number of functions built into the Sass library which we can leverage to make our own functions, mixins, loops, logic, float control more robust and more comprehensive.

In this video we gonna look at couple of those functions, particularly those which are to do with working units from the Sass library. And we gonna show you how they can be use to enhance our own type of typographic functions from the previous video. In the creating custom functions video, we created a custom px-to-rem function that, perhaps unsurprisingly, converts a pixel value into a rem value.

We started by dividing a pixel value by the base font size and then multiplying it by 1rem. Here is the reminder of what the function eventually look like. We then took this to the next level by allowing the function to be slightly more flexible, and accommodating either pixel values or plain numbers passed in his arguments by first running it through a function that strips the units.

And again here is a reminder of what that function looked like. So this is a fairly comprehensive function and it works, but we can leverage a couple of different Sass functions to make it even more robust, and handle even more used cases. Let's first look at the unitless function.

This is a built-in Sass function that returns either true or false depending on whether a unit has units. If we take a look at the Sass function reference for this unitless function, we'll see the description of the function and a couple of examples of its use. If we call unitless and passing in the value 100, the function returns true because 100 has no unit, i.e, it is unit less.

If we call unitless and passing the value 100px, 100 pixels, the function returns false because 100 pixels does have units, i.e, it is not unitless. The function will also handle errors and raise an argument error if we try to pass anything other than a number into the function.

So that's how the unitless function works, but how would this be useful to us in our px-to-rem function? Well, currently our function strips the units for many value passed in, and then converts the result into rems. But if we pass in a plain number, then we don't need to remove any unit because it doesn't have any to a ready unitless.

So we can modify our function to check if the value that we have passed is a unitless value or not. And if it is, we can go ahead and convert it to rems, if not we can first strip the units and then convert to rems. Another useful Sass function for working with units is the unit function.

This can help us when we need to perform different functionality based on what type of unit a value has. So this function returns a string containing the unit associated with a number. If we call the unit function, and parse in 100, the result is an empty string because the number 100 doesn't have any units.

If we call the function and pass in 100 pixels, the result is px. If we pass a mathematical expression to the unit function, we get a complex units. We can use this unit function in a similar way to have px-to-rem function, but with a slightly different use case.

Instead of converting numbers into rem values for use in font sizes or patterns or margins or whatever, we can create a function that converts length values, into for use in media query bright points. This is often a desirable way to write your media queries so that they apply as the size of the text changes, as well as when other factors like the browser width, or the browser height change.

So let's create a function called bp-to-em, which will convert any flexible length value to for using break points. Both this and the px-to-rem function are both inspired by similar functionality that's baked into Zurb's foundation framework. So here's our completed bp-to-em function of break point to ems. The function takes one arguments which is the value that we want to convert.

The first thing that we do is we check what units this value has. If it has a px units or it has no units at all, then we can modify our value and convert it to rems using our existing function. Otherwise if we pass in any other kind of value we'll just strip the units at the end and multiply by 1em to convert the number to units.

We can then use this function within our media queries, and any unitless or pixel value will be converted to a relative unit. There are a number of functions like unit and unitless built in to the Sass library, and combining them together with custom functions, and if/else logic like this, can be a really powerful way of creating your own library of helper functions for use across your projects.

If you're interested in a handful of other u named functions, have a search through the Sass function reference for unquote and unique ID, and see what else you can do.

