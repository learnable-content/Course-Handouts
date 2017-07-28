Today we're talking about extending Sass. This is an advanced topic, but one that can be very useful when you need to leverage more powerful programming features than Sass alone can provide. Just to be clear, we're not talking about the Sass @extend directive, we've covered that in an earlier video in the series.

Today, we're talking about extending the capabilities of the Sass compiler using the Ruby API. As I said, this is an advanced topic and would ordinarily require some knowledge of the Ruby programming language. But instead of focusing on programming some complex functionality in Ruby, we'll focus on how we actually extend Sass, the specific steps to create and use a custom Ruby function in your styles.

Even if you're not familiar with Ruby, you should still be able to follow along, and start to see the kinds of things that are possible when using this technique. First, let's have a quick chat about why you might want to do this. As we've seen throughout this series, Sass is a powerful tool that brings programming features like variables, functions, conditional statements, and loops for use in crafting of styles.

There are a number of things that Sass can't do though, such as complex maths, working with image data, or working with environment, or the file system. The Compass library use the same kind of techniques as we're going to look at in today's video, to add additional functionality to Sass to help with these more complex requirements.

Since Compass is now deprecated, you may not want to use it in your projects, but you might want to bring in certain aspects of its functionality, or add similar functionality depending on your specific needs. Extending Sass with custom Ruby functions is one way to do that. So let's take a look at what's involved.

There is a small part of the Sass documentation which talks about extending Sass in this way. And in the documentation, the Ruby function that they use is one that reverses a string. It's not very useful, but it will allow us to take the example from the documentation as a starting point without having to first learn a whole new language.

So here's the function from the documentation. It's part of the Sass script functions module, and it defines a reverse function. The def method is what we used in Ruby to define a function. And so this function reverse takes in a string then creates a new string value which is the result of reversing the string that is passed in.

It looks a little bit strange, and especially if you're not used to Ruby. This might look a little bit odd but the concept is we have a reverse function, which takes in a string of characters and reverses them. So ABC would become CBA. So now that we have a general understanding of what this function is and what it does, let's look at some more details.

There are a couple of other parts to this ruby snippet that are worth noting. Firstly, our custom reverse function is defined inside of the module, Sass script functions. And this is how we're extending the functionality of Sass with our own custom function. The second thing is that before ending the snippet, we have to declare the new reverse function and the arguments that it accepts in order for this new function to correctly be handed to Sass.

So we have this new function, how do we use it? To add a new function to Sass, we need to create a Ruby file which is just a normal text file with a dot RB file extension. Once we've created this ruby file and put our ruby function inside of it, we'll then run the Sass compiler but run it with an additional command line flag which will include this Ruby file to extend the functionality of Sass.

So I've got a simple project here with an assets folder which contains a folder for my SCSS and a folder for my complied CSS. The SCSS is very sparse and just contains a handful styles that output the word SitePoint into the body of the page via a pseudo-element.

We're going to extend Sass with our reverse function, to reverse the content in the pseudo-element. The first thing I'll do, is create a folder for the new Sass function. I'll create a lib folder within the assets folder. And within that, create a reverse.rb file to hold our Ruby function.

Within this file, we first need to require the Sass library, and that enables us to extend its functionality. This is a little bit like the import statement in Sass itself. It's like we're bringing the Sass library into this Ruby file, so that we can do something to it.

Underneath that, we'll paste in the snippet of code from the Sass documentation site. After saving the file, we can now update our Sass code to use this new function. So inside of that content property, in the after pseudo-element, we're going to output the result of reversing the string SitePoint.

But when our styles compile, we actually see the function called to reverse rendered in the browser, which is not ideal. To complete the process of extending Sass, we need to include our custom Ruby file at compile time. And to do this, we need to head to the terminal, stop the task compiler if it's already running.

And to include our Ruby file with the reverse function or any other custom Ruby file if you have multiple. We need to change the way that we run the Sass command. If we wanted to run the Sass compiler once, would use a command like this, Sass. And then the input path for the Sass file, colon, and then the output path.

To include our custom function, we'd add a -r flag, and the path to our file, -r for Ruby. This loads our new function into the Sass functions module and our styles compile without any errors. If we take a look in the browser, we should see the content has been reversed.

While this is a somewhat trivial example of just reversing some text, and it's unlikely that you'll ever want to do that in a real project. This concept of extending Sass is a really interesting one. The Sass language is already incredibly powerful. But if you want to or need to at the full power of a programming language like Ruby to perform complex functionality, then this could open up some really interesting possibilities.

