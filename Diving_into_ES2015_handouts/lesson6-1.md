Template Literals

With ES2015 comes a powerful new feature to handle interpolation restraints.Generally it is referred to as template literals.Let's get started.
Multi-line Strings

One of the first neat things about template literals is that they can spanmultiple lines.As you can see this makes for creating long strings,with new lines and white space, a very easy thing to do.So easy, in fact,that you can accidentally add whitespace when you didn't mean to.So be careful.Another super cool feature that has been a long time coming is interpolation.
String Interpolation

Given an object 'person'.We can use this in a string just like this.Awesome, much nicer to read than a series of concatenated Strings, don't you think?It's also worth noting that you can do anything inside ofthe interpolation syntax and it will simply be evaluated as JavaScript.So you can literally put anything you want in there and it will be evaluated.
Custom Interpolation

You can also use custom interpolation to create interpolatedfunctions with custom behavior.Wait a minute, what the heck is going on here?Let's take a minute to break it down.The first thing we need is a function called 'strip'that takes multiple arguments.Let's go ahead and create this function.The purpose here will be to strip all the surrounding white space fromthe multi-line string.Okay!We are actually calling this 'strip' function with a template literalas the argument.Behind the scenes the template literal is being dissected into several parts.The first is an array of strings that is splitanywhere the interpolation syntax is found.The rest of the arguments are the pieces of JavaScript themselves thathave been evaluated.Let's take this string for example.This string will produce the following arguments in our 'strip' function.So what our little 'strip' function is doing is grabbing allof the pure strings in the first argument andthen collecting the rest of the arguments into an array called 'values'.We can then build the string ourselves.Really this is what JavaScript is doing behind the scenes, andadd any extra functionality that we need to.
Moving On

Okay. Sonow we've learned about template literals.Let's put this into practice and expand on the code that we've been writing.