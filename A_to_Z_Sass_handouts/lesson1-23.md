When crafting complex functions, mixins or perhaps even your own framework or Sass plugin, it can be useful to display messages on the console to ensure your code is working correctly and being used correctly. Sass has three different methods for interacting with the console, which will cover in this episode.

they are warn, error, and debug. The warn directive prints a warning message into the console where your Sass is compiling. Here's an example, it starts with the @warn directive and then a string containing the message. If you add this code to any Sass file, the warning will be printed to the console every time you save the file.

While this is a simple way to demonstrate what the warn directive is and what it does and how it works, it's not a very useful message. Instead of having the warning display all the time, we can use it within a Sass function or within a mixin to alert the developer under certain circumstances.

For example, we might want to warn about the improper use of some arguments, or to add a deprecation warning about the use of an old function. So in this example, I've put a function that we created in a previous screen cast that converts pixels into rems. Let's imagine that this function is part of a Sass library, or part of a framework that is used on multiple projects by multiple developers.

Maybe like a small version of the Bootstrap library or the foundation framework. Let's say that we're the developers of this framework and we want to rename one of the functions, but we don't wanna create a breaking change in the code. We don't want all other people who use our wonderful library or wonderful framework to suddenly have to go and change all of that code just cuz we made a small update.

So the px-to-rem function is a bit of a long name. And instead we might want to rename it so it's just called the rem function. If we just rename the function, then any instances in the code where that function is used will now throw errors. So to ensure that our new shortened function name doesn't create this breaking change, we can create a new function with the same name as the old one which calls the new one.

So we take our existing px-to-rem function. We rename it to now be called the rem function, but then we create a new function called px-to-rem which calls the rem function. And to let the developer know what's going on behind the scene. So they can be aware of what's changed.

We can then add a warning message into the px-to-rem function. So for example, the px-to-rem function has been deprecated and will be removed in a future version, use the rem function instead. Now, when we use the old function, there are no errors thrown, but the developer is alerted to the fact that there is a new shorter-named function that they can use instead.

In a similar fashion to the warn directive, the error directive can be used to display a custom error message in the console. It looks like this. We have @error and then a string of texts which describes the error in question. One difference between a warning message and an error message is how they display on the console.

But the key difference is that the error directive will stop the compiler at the point of the error. Whereas the warn directive is just a warning and the compiler will continue and keep going. And such, the erro directive should be used to alert the developer something fatal has happened with something that needs to be corrected before proceeding.

So a classic example of this is when using incompatible values in a functional mixin. Let's take a look at an example. Using our rem function from the previous example, we might want to throw an error if If units other than pixels are passed into our function for conversation.

Because if they were, they wouldn't give us the results that we're expecting. So to handle this, we could add a conditional statement before the main body of the function to catch any values that are not unitless or not in pixels. If we try to call the rem function with an value now, our error is thrown.

To make @error message even more helpful, we could output the value which cause the error in to the message using some sass string interpolation. Now that is much more useful. Finally, the debug directive can be used when you are in the process of developing your own functions and mixins.

This is a bit like the console.log function used when developing in debug and code in JavaScript. Like the warn directive, the debug directive doesn't stop the compiler running, and it just prints out a message into the console. Here, we're printing out the value passed into the function before we strip its units, and then again, afterwards, to ensure that we see the expected behavior.

So, we've just added a couple of lines into our rem function. The first one, prints out the initial value then we stripped the units then we printout the modified value. Instead of writing out a debug message, it's also a possible to debug just a variable or the result of running an expression.

So if we debug a variable value that will print a value into the console or if we debug an expression like (value / $base- font- size) * 1rem, it will print out the result of executing that expression. Each of these directives the warn, the error, the debug are useful in the rem write.

But when they're combined together like these, it allows you to create some really robust code that clearly communicates back if it's being used incorrectly or sub optimally. Warn and error are particularly useful if you're developing something for many people to use, if you're developing a framework or a boiler plate, or something like that.

Whereas the debug directive will be really useful, whether you're working solo, or working as part of a large team.

