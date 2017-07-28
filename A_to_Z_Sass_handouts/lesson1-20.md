**Typography** is not just about choosing some fancy fonts. Good typography is all about having a system. Design is not decorating, it's about solving problems in a visually appealing way. And the best solutions are often found in structure, order, rules and repetition. Sass is an ideal partner for creating great typography, because we can use it to create a repeatable system through variables, functions and mixins.

In this video, we're gonna look at a couple of plugins for Sass that leverage custom functions and mixins to build a flexible typographic system. We're gonna look at two, Modular Scale and Sassline. To bring some order and hierarchy to your heading sizes, you could consider using a Modular Scale.

In this typographic system, you choose a base font size, such as 1em, and a ratio or maybe even a series of ratios. To calculate a series of font sizes that work within the scale, you multiply each number by the same ratio. So let's take an example, starting with a base of 1em and a ratio of 1.5.

The next size up the scale would be 1 times 1.5 which is 1.5em. The next size up would be 1.5 times 1.5, which is 2.25ems. To create smaller numbers, you divide by the ratio. To create the first size down from the base, which is 1em, you would divide 1 by 1.5 to get 0.667em.

To get the next size down, you divide this by 1.5 and so on. There's a web based tool at modularscale.com, which is a great way to visualize this scale and to experiment with the values which you can then copy and paste into your projects. There's also a Sass plugin that you can install into your project for an even tighter integration, but that requires a little bit of set up.

But since you're here, let's take a look at that. So to use the Sass plugin head to the GitHub page and chose your favorite method of installation. I have a simple project set up here, which is already using the power package manager. So I'm gonna install using Bower.

As long as you have Bower installed, you can run the following command from your terminal within your project. Bower install modular-scale --save-dev, this will install the modular-scale as a dependency of your project. And to use this in your Sass, you first need to import the modular scale library.

Now that the library has been imported there is a small amount of setup required, so that we can start using the modular scale function. So I've created a type.scss partial here, which will use to set up all of the typography settings. It's always good to keep things separate and keep things organized.

So the first thing we're gonna do is create a modularscale map variable which contains the base font size and the modularscale ratio. For the ratio, you can either manually add in a decimal value or you can use one of the predefined ratio variables. A list of these can be found on the modular scale GitHub page.

So I'm gonna use the one called the golden ratio and I'm gonna add that into our Sass code. And having configured this, having set up the modular scale variable, we can now use the modular scale function to output values in our Sass. So I've created a series of selectors here for our heading styles, and the default body style, the default body copy.

So that we can see both going up the scale and down the scale. I've got normal font-size for the body and we got some small font-sizes and then some large font-sizes for the headings. And for each of these, we can set the font-size using the modular scale ms function.

And this function takes a numeric parameter that determines how far up or down the modular scale we want to go to calculate the font size. So each of these is just a whole number either positive or negative, positive numbers for going up the scale, negative numbers for going down the scale.

Having set these type sizes up we can save, switch and refresh the browser to see what we've got. And having set everything up properly, you can now experiment with either the base font size. Or the ratio to see what different combinations of settings yield just by adjusting two variables, which is pretty handy.

The second plugin in we're gonna look at is called Sassline. This is another tool that helps with managing your typography, but specifically is all about handling setting type on a baseline grid. It also includes a responsive modular scale, which is what we've just looked at. And contains a whole load of other typography best practices.

And tuns on some of the really nice OpenType font features such as Ligatures Oldstyle numerals and Kerning. if you like the idea of using a baseline grid and having sleek looking topography as well as the solid starting point for a new project, Sassline looks like a great option.

It's not the simplest thing to introduce to an exiting project as it also comes with it's own research and its own grid. But given the way that the plugin has been structured, you could just import the variables and mixins and go from there. So head over to the GitHub page, and download the project as a zip or clone it to your local machine.

In order to build and preview the demo, we first need to install the project dependencies using NPM and Bower. Which you should already have installed, if you worked through the first example on modular scale. You will need these tools in order to try out Sassline and so if you need to install them, you can head to the Node.js website or the Bower website.

Once you've those installed though, we can continue. So to test the project out, we first need to install the dependencies. So in a terminal window for the Sass line demo project, we can run npm install and bower install. We'll speed things up a bit because this can sometimes take a while.

But once the dependencies have finished installing, you should see a success message. The Sass project uses a gulped task runner to compile the Sass and to run a local development environment. So also make sure that you have gulp installed and then, run gulp serve from the command line.

This will launch a local server which you can access via local host:1234. And if you browse to this URL, you should see this Sassline demo page. This provides a great base for your new project and is a fully configured Sassline project using all of the Sassline variables and mixins.

For details of how all this work and how they will fit together refer to this blog post with the link on the screen which is written by Jake, the plugin author. Given the web is predominantly made up of text, it's hugely important to design legible text in a system that works, both for you and the users of your projects.

The Modular Scale and Sassline project, can help you do both of those things with ease.

