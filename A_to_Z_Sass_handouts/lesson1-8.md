**Mixins** are a Sass feature that enable blocks of code to be reused with slight variations throughout an entire codebase. They're a really powerful feature and they're a core tool in writing modular and maintainable code. In this episode we'll go over a whole heap of handy mixins to help you out in all sorts of aspects of crafting styles for many different types of projects.

So in this video, you'll learn the anatomy of Sass mixins, utility mixins for styling placeholder text and selection text, mixins for centering different types of elements, and mixins for hiding elements. There are a number of different bits and pieces that make up a mixin. So first, we declare the mixin with the at mixin directive, followed by a name for the mixin.

The mixin name is optionally followed by a set of parenthesis where we can define any input parameters. These are then made available as variables within the mixin to enable the output CSS to change based on the input values when the mixin is called or included. When the mixin is used, the styles within the body of mixin are output where the mixin is called where the @include statement.

So it's kind of like the styles from within the mixin are copied and pasted automatically by Sass wherever they're called. Some mixins may output other selectors instead of just outputting properties and values. To do this we can create a mixin with the @content directive in the body of the mixin.

When this type of mixin is included we use curly braces to define what the content of the mixin is going to be, and the braces dictate where it starts and ends. So our hover focus active mixin used in this way, would then compile into the following CSS. Mixins are very useful, and they can be a great time saver.

But when you're first learning Sass, sometimes it can be a bit hard to know what you might use them for or how you might start to think in this way. So to help with that, here are a handful of helpful mixins and examples of how you might use them throughout a project.

When styling selection text, we need to provide two separate blocks of CSS to handle the different vendor prefixes from the selector. Creating a mixin allows us to set the selection text colors just once and then have them replicated in both selectors as necessary. Form input placeholder selectors are similar to selection text selectors in that they require different vendor prefixes in the selectors.

And that means that each browser needs to be targeted separately. In this mixin, the placeholder styles can be defined once and then passed to the @content directive in each of the four input place order selectors. Centering elements is a very common practice and it can be accomplished with fairly minimal CSS.

But it's such a common practice that it's often simpler to write a single line instead of three or four even if they are quite well known. So here we've got a mixin for centering a block element with margin auto. Here we've got a mixin for performing absolute-center, which will do both horizontal and vertical centering in anything above IE9.

And then finally we've got a vertical center which doesn't do anything horizontally but will vertically center in element within its container using a combination of absolute positioning and transform translate. Creating mixins for common styles and common patterns like this could be considered an abstraction a bit too far.

And to some, it may be seen as less meaningful and less readable code. But use your own judgment and just be consistent in whichever method you choose. There are a number of approaches for hiding elements while still allowing them to be visible to users of screen readers. This mixin is taken from the HTML5 boilerplate and is a solid approach for creating something that is visually hidden.

When hiding something we want to really make sure that it's hidden, so I've included a bang important after each of the declarations here to ensure that the element is definitely not visible to any sighted users. This is really the only time that such liberal use of important makes any sense.

Try to avoid it for getting out of specificity trouble. But for something like this, when we wanna definitely make sure that something is not visible, it does make sense. So I keep all of my mixins in their own mixins.scss partial in each of my projects to keep everything together and to provide a logical place for any new ones to be added.

If you like the sound of having a library of mixins to lean on from time to time, but you aren't too keen on having to write them out yourself, then there are a couple of Sass tools out there, that provide exactly that. We'll be covering the library Bourbon and Neat in a future video but you could also checkout Compass or Scout which both provide a whole heap of mixins for all sorts of day to day tasks.

