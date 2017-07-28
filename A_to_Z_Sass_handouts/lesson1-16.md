Today, we're gonna talk about Sass performance. This is a tricky subject and one that is often very specific to each individual project. It's dependencies, the local or production environment and the scale of the project, and perhaps even the scale of the team. However, performance is a really important subject.

So, it's something I wanted to try and tackle. That being said, I wouldn't call myself a performance expert. I'm sure there are people much more qualified to talk about much more technical applications of performance. But we're gonna cover it from a Sass and CSS side of things today.

And to do so, we're gonna break this topic down into two main areas of discussion. How to improve compiler performance for improved developer happiness and faster workflow. And how to write Sass code which outputs clean and performant CSS. Having a solid workflow when writing code is really important to make sure that you can work as quickly as you need to or as you want to.

Sass needs to be compiled into CSS before it can be read by the browser, as I'm sure you're aware. And this compile step can sometimes become a little bit of a bottleneck and actually starts slowing down your development. On a recent client project, which I inherited from another agency in a pretty terrible shape of being honest, the compile time for the Sass was frequently taking over 14 seconds.

On a similar scale project on my own, compiling the styles takes less than one second. So why was there so much difference here? On the client project which will remain nameless, it had the following set up. It was using Ruby Sass, we were using the Compass mixin library.

There were two separate compiled stylesheets, there were 67 partials, and we were using the Grunt task runner for actually running the compiler. On my personal project, which is an online food website for ethical and sustainable food, you can find it at thefoodrush.com, it has the following setup. We're using Node Sass, we're using Autoprefixer.

There's one compiled stylesheet. And at the time of this recording, there's 42 Sass partials and we're using Gulp for compiling the Sass. While the client project has more partials and one more compiled stylesheet, I believe that the major bottleneck in this compile process was using the compass library and the use of Ruby Sass.

Not that there's anything wrong with Ruby Sass, but it runs a lot slower than Node Sass, which is what I'm using on my personal project. Compass is a library full of all sorts of handy mixins and functions for working with Sass. A little bit like Neat and Bourbon that we looked at in a previous video in this series.

The majority of the Compass library provides CSS3 mixins for handling vendor prefixes across different browsers. Compass modules could be loaded on a case-by-case basis. Or you can include the whole library in one go, which was done on the client project. The only Compass mixins that were being used were for transitions, transform, opacity, and box sizing.

And these are now widely supported without any vendor prefixes at all. And if prefixes where needed to support particular range of browsers, it wouldn't be too hard to add these manually even for just these four properties. We could create a custom mixin as needed or we could use an automated tool for prefixing like auto-prefixer.

The second change to improve the performance of compiling this project would be to change from using Ruby Sass to LibSass, which is often done through the Node Sass wrapper as part of either Gulp task or a Grunt task. LibSass is a C or C++ port of the original Ruby Sass engine, and it runs incredibly fast.

If you refer back to the episode about Grunt and Gulp, you'll be able to see an example of the difference in compile time for exactly the same code. The Ruby Sass with Grunt compiled in 1.5 seconds, and the Node Sass with Gulp compiled in 10 milliseconds. Now this isn't anything to do with the difference between Grunt and Gulp, it's the difference between Ruby Sass and Node Sass.

But go and check out that video for practical step by step instructions on how to use and set up either Grant or Gulp to compile your Sass. For more details and some more cold hard fact and figures about compile times of various different versions of Sass and other pre-processors, there's a post on Opinionated Programmer, which is really great.

And there is a link on the screen here, and there'll be a link in the description as well. So to wrap up this part of the discussion, there are really two takeaways. To improve the performance of your compiler, reduce the amount of plugins or libraries that are used in the project.

And try LibSass or one of its common wrappers for a super fast compile time. Moving away from the idea of performance in terms of speed and efficiency of our workflow, let's turn our attention to writing Sass that compiles to compact, clean and clear CSS. I've spent many hours writing CSS and have tried a number of modular coding techniques, naming conventions, methodologies like OOCSS and SMACSS.

And I've experimented with both @extend and @mixin a lot. It would probably take hours to go into fine detail about what I've learned on the topic. And so I've tried to distill it down into five tips for writing Sass that outputs CSS without too much bloat. Firstly, read your compiled CSS.

When optimizing anything, it's important to know what you're optimizing. Being aware of the CSS that's being generated from your Sass is sometimes all you need to know whether your generating code is compact and lightweight, or a bit of a bloated mess. If you're working on a large project, reading through the whole compiled stylesheet might be a little bit impossible.

So you could just experiment with some snippets of code on a Sass meister gist, suggest or on code pen just to check the difference between the two. But it's really useful to be aware of the CSS code that your Sass is generating. The second tip is to avoid overqualified selectors and avoid nesting.

Specificity is something to keep in mind when writing Sass or CSS. The more specific the selectors you write, the more specific the selectors you'll need to override previously declared styles. This can lead to many more lines of code and can make life really difficult for yourself and your other members of your team.

Avoid over qualified selectors like a.button or div.main, as this limits the reuse of these styles. If you think that you need to modify existing styles for specific elements, adding a modifier class is usually a better approach than differentiating by element type, which can be very limiting. It's almost impossible to read a blog post or watch a video about Sass without hearing about the warnings about don't nest too deeply, but it's worth reiterating.

Don't nest too deeply. Nesting selectors can lead you into a false sense of security as you're only typing something very short, but then these selectors compile into something much longer, and much more complex, if you've used a lot of nesting. I once inherited a project which had a home page file, which was styled just for the home page, and it had a thousand lines of Sass.

And the first line of code was body.homepage and every other line of code was nested inside of that. Which means that these 1,000 lines of codes would only ever apply to a page whose body element had a class of homepage. To my mind, this is the complete opposite of a modular and reusable code, and it was an absolute nightmare to maintain.

Tip 3 is you be wary of mixins, but don't worry about it too much. Mixins are used to generate similar patterns of code throughout a code base. And they often get a bad reputation because they generate multiple lines of identical or almost identical code, depending on how they're structured and how they're used.

My advice is to be aware of the mixins that you use to ensure that they don't generate masses and masses of unnecessary duplication. But don't worry about them too much, because this kind of duplication can be heavily compressed as long as your server has gzip turned on. And that apparent bloated CSS will actually end up very compact.

Tip number 4 is to avoid using extend. This has almost become a Sass meme in the front end development world. It's a popular buzz phrase among Sass users, which is, don't use extend. We've talked about it in a previous episode, and we even talked about the pros and cons length in that episode.

So without revisiting the exact same arguments, to improve the performance of your compile times and your generated CSS, I would generally avoid using the extend for anything other than extending utility classes like clear fix. Tip number 5 is to consider using multiple compiled stylesheets. This can sometimes seem a little bit contradictory to the usual advice which is import one single file which is a concatenation of multiple files into one to reduce HTTP request.

Whilst that can be good advice with the advent of HTTP 2, this is perhaps less of a concern. But in some cases, it's better for performance to have multiple compiled stylesheets that are loaded on different pages of a large website or application. Let me explain what I mean by that.

So imagine you have a site with a whole load of content and informational pages, and maybe an online shop. The shop has got a whole load of pages, and a whole load of templates, and a whole load of steps for the checkout process for viewing the products, putting them into your basket, going through the checkout, all that kind of thing.

And these pages, the shop pages, would no doubt have a significant amount of custom components and styles that aren't used throughout the rest of the website. And these shop pages are probably only seen by a small percentage of the site's visitors, if the shop is just one part of the larger site full of content.

So conventional wisdom might say that combining scripts and stylesheets into as few files as possible will reduce HTTP requests. Which is true, but if your single stylesheet is full of code that only gets seen by a small number of your users, would it not make more sense to separate that out into two smaller stylesheets?

This can also have caching benefits too. If you got one massive stylesheet, and you change a single line or a single property, then you have to break the cash for that file, meaning, that all of the users need to re download all of it. Whereas, if you have stylesheets that are split up into different files for different sections of the website, if you need to make a small change to just the shop, then only people who visit the shop pages and request the shop CSS file will need to redownload that.

So there can be some benefits here. One last bonus tip, don't forget that making CSS perform better, either for developer happiness or for your users, is kind of a micro optimisation. Get the low hanging fruit out of the way first and then tackle things like CSS optimisation second.

Those low hanging fruit would be things like turning on Gzip on the server, making sure all the images are compressed. Make sure your leveraging caching, and make sure you compress and minify all of your assets, and even consider using a CDN. So there we have it, a selection of a performance related tips.

These aren't necessarily the Holy Grail of making a super fast website. But they're certainly some good things to keep in mind when you're writing your code, or working as part of a wider team.

