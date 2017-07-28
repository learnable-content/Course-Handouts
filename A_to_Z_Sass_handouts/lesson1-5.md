In this episode, you'll learn all about **extends** and how they're different to **mixins**, how to create and extend placeholder selectors, and about some of the pros and cons of using extend in real projects. To understand extending selectors, let's first have a quick recap of the mixin directive.

I've got an example here with a mixin that sets up some default font styling. It makes all the text uppercase and spaces the letters out just a bit. To use this mixin, we declare @include followed by the name of the mixin within any other CSS selector. Having done that, the styles from within the mixin are then output at the include point when the CSS compiles.

In the HTML, I've got three different elements, and I want to apply the mixin to each of them. Now this example is quite compact, but imagine the selector has been used in multiple Sass files or even being separated by many lines of code in the same file. I'm keeping it all compact here, just so that you can see what's going on, but this is a slightly contrived example.

When using mixins, the code is duplicated within each selector. And in this case, the generated CSS will have the same number of text transform and the same number of letter spacing declarations for as many times as we include the mixin. This is all well and good, but it can lead to a lot of duplication in the compiled CSS, even if we're not having to type it all out manually in the Sass.

Now let's take a look at using extend instead. Extends are used to have one selector inherit all of the styles of another selector. And the compiled CSS is a comma separated list of all of the selectors that share the same properties. So, instead of creating a mixin for the uppercase and letter space text, we could create a class instead.

And then we can have all of our other selectors inherit these properties for our extend. Again, do mention that that these selectors are all separated by many lines of code or in different files. Just keeping it all compact, so that you can see everything in one screen. So the major difference between extend and mixin is what is output in the CSS by the compiler.

In the previous example, we looked at creating a class, which had styles inherited by a number of other selectors throughout the code base. But what if the uppercase-letter-spacing class was never designed to be used on its own and never intended to be added as a class to any of the elements in the HTML?

This would actually mean we have a redundant class in our CSS, which is never gonna be used at all. So in this case, we can create something called a placeholder selector, which is never compiled into the CSS. But its properties can be inherited by other selectors by using extend.

Placeholder selectors are defined with the % character to differentiate them from other selectors like classes with dot or IDs with hash or pound sign. To rewrite our previous example with placeholder selectors, we would use the following snippet. When our Sass compiles, there is no selector generated with the name uppercase-letter-spacing.

But this silence selector can still be used within the Sass. Adding the extends back in, we now get the following result in the compiled CSS. So when extending normal selectors like classes, the selector being extended will be compiled into CSS. But when using placeholders, only the result of the extend will be generated.

A great use case for extend is when applying clearfix to prevent container collapse when building floated layouts. For more information on float and clearfix, check out the video on float in Season 1 of A to Z CSS. So instead of creating a clearfix class, we can create a clearfix placeholder selector.

And then instead of adding classes to the html, we can just extend the placeholder where necessary. I used this technique myself to avoid cluttering up the HTML with utility classes, and I found this to be a really great use case for extend. So this extend thing sounds pretty great, right?

By using extend everywhere, we can reduce the amount of code that's generated in the CSS. We can have a super lean, super efficient comma separated list of all the selectors that share the same properties, right? Well, you may be able to tell from the tone of my voice, well, maybe not.

Sometimes people complain that they don't get my sarcasm. Maybe you can tell that using extend is not always a great idea. But there are some benefits. So, what are the pros? Well, we've already seen the main one, which is that the compiled output is fewer lines of code.

All the shared properties are applied to one automatically generated comma separated series of selectors. Another positive reason for using extend is that you can reduce the number of classes applied to an element in the HTML. Because you can have a single class inherit the behavior of multiple classes.

This can help bring a bit more meaning to your class names. So instead of div class ="col medium-4 large-6 last", we could have something much shorter and something more descriptive, like div class=" latest-posts". Which is an extension of the col class, the medium-4 class, the large-6 class, and the last class, and then all the other styles underneath.

But there are some downsides to using extend. And there's really a balance to be struck between meaningful class names or descriptive class names and how easy the code is to understand when it's being read by yourself or any of your teammates. Reading the class name latest-post gives a great sense of the purpose of the element.

But you'd have to refer back to the CSS or to the Sass files to find out what it actually does and what it's actually comprised of. Having to look up all of this information can take time, whereas the first, albeit less attractive, markup with many classes at least shows all the various bits and pieces that make it up at a surface level.

The second major drawback of extend comes with complex projects, which have many extends or even nested extends. Unfortunately, we take a very long and very complicated example to illustrate this point. But the general gist is that extend can easily be misused, and if extending complex selectors can actually lead to a very bloated code base and very long compile times.

Thirdly, when your CSS is minified and compressed with gzip, any duplicated properties that are generated by a mixin will be compressed to the point that the benefits of using extend are actually negligible in many cases. A final downside is seen when inspecting and debugging elements in the developer tools.

Seeing a huge list of comma separated selectors can be a bit tricky to navigate. And it takes up a lot of space in the inspector, making things harder to debug efficiently. This is not to say that you should never use extend. Just be aware that it's not a magic bullet.

And there can be some side effects. I thought it was amazing when I first discovered it. And that ended up biting me in a large scale project. And I've learnt my lesson since then. But if you do see the benefit of extend, and you want to use it most effectively, here are some tips from Sass guidelines.

Use extend on placeholders primarily, not on actual selectors, like classes. When extending classes only extend a class with another class, never a complex selector. Directly extend placeholder selectors as few times as possible, and avoid extending general ancestor selectors, such as descendant selectors or general sibling selectors, as this is what can cause selector explosion.

This is some very good advice, and there's a lot more of it in the rest of the Sass guidelines. You may find them a little opinionated, but there's definitely a lot of wisdom in them too.

