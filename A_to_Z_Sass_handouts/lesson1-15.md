Over the first half of this video series, we've been looking at some of the major features of Sass and a number of practical examples of putting them into action. Today, we're gonna look at two smaller features of the language that have a very specific use case. In this video, you'll learn all about how to silence compiler errors when extending selectors that aren't compatible or not found.

And how to make default variables that can be overridden at the later stage. We covered the @extend directive back in episode five, and covered extending classes and silent placeholder selectors. Here's a quick recap of how it works. I've got an example here with a base class of message which sets up some visual characteristics for a notification.

If our project needs additional types of message, perhaps for a success message or an error message, we could create additional classes and then have them inherit the base notification styles via @extend. This produces a comma separated list of selectors in the compiled CSS that share the same properties, the ones that were extended.

And then additional selectors that contain only the unique properties or values. But imagine the situation where this message module is being used from a third-party library or framework. Perhaps this unintentionally is removed or perhaps it's loaded in the wrong order. When our Sass compiles, it wouldn't be able to extend the message class and it would throw an error.

To mimic that behavior, I'm going to comment out the message class and save the code. The compiled CSS now contains the error message that the success message class failed to extend the message class. To silence this error and to have our Sass code fail more gracefully, we can add the !optional flag to the end of the @extend statement.

This prevents the compile from failing and it allows the rest of the code to compile as normal, and we can continue on our merry way. However, I'm not so sure that this is a great idea. One of the great things about Sass is that any errors in our CSS are caught by the compiler.

If we make a mistake, we make a typo, or whatever it might be, we can fix that problem. And ensure that every style that we write will be correct and will be valid and will, eventually, be painted to the screen. Having errors go undetected like this, using this !optional flag, doesn't sound like a great idea to me.

But maybe there's something I'm missing here. So if I am, just get in touch and let me know. Another flag available to Sass authors is the !default flag. This is used in conjunction with variables and allows a variable to be given a value if it's not already been defined.

If it has already been defined, it will use that value instead. This is a little bit hard to get your head around, so let's take a look at an example of using variables in this way. Imagine we're creating a starter template for a new project. And a number of the key settings for the site are controlled via global variables for things like the primary and secondary colors, the base font size, and the heading sizes.

We would normally create separate partials for the variables and then the different components and pages and stuff like that. But here, I've kept them in the same file so that you can see everything on a single screen much easier. So here are the series of variables with their initial values.

If we wanna override any of these values, we can just re-declare the variable further down the file and change that value. Again, I'm keeping it all in one screen here so that you can see everything. This could potentially be in separate files. The variables further down the file, or lower in the source order if we wanna get technical, override the ones above.

However, if we make the initial settings all default variables, the source order doesn't have any effect. And these variables without the !default flag will always win. Any default variables that aren't re-declared just use their default value. So these two features aren't the most powerful or even the most commonly used Sass features.

But they're often used in CSS frameworks and boilerplate code. You might have seen them around and about but not been entirely sure of what they do. Well, now you know.

