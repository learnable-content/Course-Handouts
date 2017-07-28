**BEM** is a system of naming classes that encourages the good practice of writing modular code. It can really help to bring structure and meaning to the way that we name things, which is often quite a difficult practice. And BEM is something that I use consistently in my day to day client work.

It can be used with or without Sass, but BEM and Sass are a great combination. In this episode, you'll learn what BEM is and what it stands for, how to leverage the Sass ampersand with BEM, and some BEM best practices.

BEM is a naming convention to help add structure and meaning to class names. It stands for **Block Element Modifier**, and it's a great system for building flexible and modular code by creating a series of components. It's a smart way of naming your CSS classes to give them more transparency and meaning to other developers. They are far more strict and informative, which makes the BEM naming convention ideal for teams of developers on larger projects that might last a while.

Thinking about your code as a series of components rather than on a page by page basis can help you work faster by building a system of reusable bits and pieces. This is then easier to maintain and helps the design of a project look and feel consistent. The BEM Syntax can look a little bit strange when you see it for the first time because it uses a notation of double underscores and double dashes to indicate whether a particular class is for a block, for an element, or a modifier.

So the syntax looks like this:

```
```

We use a fairly standard looking class name for each block. The elements within that block or within that component are denoted by a double underscore. And then we have modifier classes, which are given a double dash between the name of the block and the name of the modifier.

It may look a little bit more ugly and it is a little bit more typing but it can really help to make your code more readable, so do bear with me.

Let's take the example of a common design pattern to illustrate how all this works. And let's look at something called the media objects, which was popularized by Nicole Sullivan of OOCSS fame.

We can refer to this whole thing as a BEM block, and we might give it the class name of media. This media block has two parts to it. There's the media partner which is often an image but it could be an icon or even a video, and then the text content to the right-hand side.

We can refer to the image and the text as elements within the media block, and with the BEM syntax could be written as follows. Perhaps we'd like the flexibility of a media block with the image on the right and the content on the left instead. For this we could use a modify class, which is added to the parent block.

So you'd always have the block class and the modifier class added at the same time. This class can be used to modify the style of the elements within. This method of naming classes works very well, and I use it a lot in my day-to-day work. But one complaint of this syntax is that the class names are a little bit long, which can get a bit tedious to type.

And some people find them a bit difficult to read. Well Sass may just be able to help us out here. In the previous episode we looked at the Sass ampersand character, and how it can be used to represent the parent selector when nesting. The ampersand has another use and can be particularly handy when working with BEM.

Going back to our previous example, here is the full code for our media block in normal CSS. Media is repeated in each of the selectors, and repetition is something we often want to reduce in our code. Instead, we can rewrite this syntax with nesting and the Sass ampersand.

This strips out all of the references to media and replaces them with the ampersand character. Now normally, nesting selectors like this would produce descendant selectors in the compiled CSS. But using the ampersand as the first character in the selector does not. And this Sass snippet will actually produce exactly the same output CSS that we looked at earlier.

So nesting in this way provides all the benefits of nesting, which is to group our code together and demonstrate the hierarchy of all the different elements. But without the downside of generating overly or unnecessarily specific selectors. So this may sound like a perfect solution, but unfortunately there are a couple of downsides.

One of the biggest issues with using BEM with the Sass ampersand as we've just looked at, is that your codebase becomes less searchable. Instead of being able to find and replace or even just find a selector by name. You can only ever search for the block part, or the element part, or the modify part of the class name.

Another downside of this syntax is that, if you have a lot of CSS that spans across many lines or if you have lots of elements within each block. You may find that the parent selector isn't visible when you're working on a particular part of the code further down the file.

This could lead to confusion and actually makes the code less easy to read. If you like this nested BEM syntax using the ampersand, but you still want a searchable codebase, one thing you could do would be to add a comment before each selector, which could then be searched for.

Another tip for working with BEM is to really think about how you create your modules or your blocks so that they can be kept as compact as possible to improve readability. Each block should be a distinct component rather than just uses a naming prefix for all of the classes that are used on a particular page.

So components are things like buttons or registration forms, or items in a grid of products, or portfolio pieces, or perhaps, pagination, or social icons. Anything that is distinct that could be made up of a number of smaller elements. And then they can be reused across an entire site.

In the past, I've made the mistake of taking a parent class like home, or products, or something like that. And using that as the base block for all of my BEM glasses. This can then lead to a lot of really long and complicated class names with loads of underscores and loads of dashes.

And it just gets a bit of a mess quite quickly. And very tedious to type, as demonstrated by this example here. In this case something like the home_features-item should really be its own component, perhaps just called feature. Which has its own elements and modifiers. Naming things is really hard.

But using a system like BEM can really hope to focus your thinking and add meaning and structure to your code. Which is important for maintainability and readability. And will be a great help to you, and your fellow teammates in the future.

