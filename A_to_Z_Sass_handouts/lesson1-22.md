We've been using Sass variables throughout this series. We've discussed the various different data types. And you should now be comfortable managing all sorts of different values across your styles. One aspect of using variables in any programming language is variable scope. Sass is no different and in this video, we'll cover all aspects of variable scope in Sass.

We'll look at the default scope of variables, we'll look at the scope in nested styles, scope of variables in functions and mixins, scope in if and else conditions, and finally, variable flags. When defining variables in Sass, they're come in two different forms of variable scope, global scope and local Scope.

When we talked about scope what we basically saying is, which aspects of the code a variable is contained within? Some variables can be used across the entire file, these are known as being in global scope. And some variables can only be used in certain locations, and this is set to be variables in local scope.

So, if we declare a variable outside of any selectors, any functions or any mixins, it's in the global scope, and it can be used in multiple places throughout the code. Here, my color variable is being used as the background and the border color of my box and as the color of the text in the H1.

This is probably the most common use of Sass variables. And it enables you to use the same value across multiple partials and in multiple selectors, and have a single line of code to change if you wanna adjust the value. I could change the color from red to blue, and that change is reflected in every single place that the variable is used.

When using variables in nested selectors, the nesting creates a local scope for any variables declared inside the parent selector. If I move the color variable declaration into the box nested selector, everything still works as it did before, but the color variable is now only available within the box class.

If I try and use this variable outside of the nesting structure, Sass will throw an error because that variable is undefined for that part of the file. Similarly, when working with nesting and variables, child selectors have access to the variables in parent selectors as we saw before. But parent selectors don't have access to variables in their child selectors.

This shows us that each selector in a nested chain creates its own local scope. Even moving the order of the styles around, shows that it's not the source order that determines which variables are applied. It's the scope that has the biggest effect on what is eventually rendered in the browser.

Just like scope in nested selectors, functions and mixins also create their own local scope. If we create a mixin that outputs a color property from a variable locally defined in the mixin, we'll see that this local variable will always take precedence to any external variables even if they have the same name.

To make this mix in more flexible, we could define it so that it takes a color parameter. Again, the local scope of the mixin variable will always apply even if the variable name is used elsewhere. The same can be said for functions. We could rewrite this mixin as a function instead, which returns the border color that is gonna be set.

This approach would be a little excessive for setting a border value in a real world project, but I'm just using it to briefly demonstrate how variable scope works in functions and mixins. Like in many programming languages, logical flow control, which is if/else and else/if, also creates local scope.

But there are a couple things to watch out for here, so let's take a look. So the following snippet of Sass conditionally sets that color of an H1 tag. We have a local color variable defined inside the selector, and then a condition that changes the color. If the condition is true, the color is blue.

If the condition is false, the color is green. This is all good and logical. But something strange happens if we move the variable declaration out into the global scope. Now the text color is always red. This is because, the global variable is not overridden in the local scope of the if/else block.

To make this set up work we have to move the setting of the color property inside the conditional statement. Because the braces of the conditional create a local scope, we need to declare the property and value within that local scope if we expect to see the right colors.

It's a bit tricky to get your head around at first, and it's probably the least intuitive aspect of variable scope in Sass. In a previous video, we looked at the Sass optional and default flags. There is one more that's useful to look at when discussing variable scope, which is the global flag.

This can be appended to the declaration of any variable in any local scope to make it a global variable. If we go back to our example from earlier, when Sass was throwing errors about undefined variables, we can illustrate how this works. In this example, we have a locally scoped color variable within the nesting of the box selector.

Currently, this variable is not available outside of this nesting area. So the use of the variable in the body tag selector below is throwing an error. If we add the global flag to the end of the declaration, the variable is now in the global scope. And this is then made available to the body tag and the background of the page is given a faint tint.

The rules of variable scope still apply. And if we redefine the color variable elsewhere in a local scope, it will override the global value. If a second global flag is added, then the last one is used and the global scope is the overridden. So this concept of variable scope is a very important one if you wanna get a complete understanding of how variables work in Sass.

It's a little bit advanced and a little bit tricky. But if you do want to master the Sass language, it's definitely a useful thing to get a grasp on.

