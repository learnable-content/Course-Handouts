**Color** is hugely important for adding life and visual interest to a project and is an invaluable tool for highlighting parts of the interface that a user can interact with. In this practical episode we're going to talk all about manipulating colors programatically with Sass. It's quite common for a project to use a palette of colors for headings, body copy, links and buttons among other things.

When designing the visual style of the site, tools like Photoshop or Sketch may be used. But sometimes, working in the browser is the fastest way to experiment as all the colors and the fonts or the type sizes can be changed all at once by leveraging Sass variables. Often when experimenting with color, a front-end designer may want to just tweak the colors a little bit to get the right tone or the right amount of contrast.

Sass has got a number of color functions built into it that can help do just that. Each color function takes a base color, which can be any valid color format, such as a name or a hex code or an rgb value or an hsl value or even another Sass variable. That base color can then be modified by a certain amount, often declared as a percentage.

Let's illustrate some of the most useful color functions with a practical example. Here I've got a box with a background color, which is defined by the variable $base-color, which at the moment is set to AtoZ CSS pink.

If I wanted a slightly lighter shade of pink, I can use the Sass `lighten` function. Or if I wanted to darken it slightly, I can use the `darken` function. The color could be more saturated or even desaturated, too. We have other options available as well. We could invert the color, or make it grayscale, or turn it into its complementary color, which is its opposite color on the color wheel.

Finally, we have a number of color functions available for making a color more transparent or more opaque. And these take a decimal number rather than a percentage, just like when setting the alpha channel in rgba or when setting a opacity.

It's not uncommon to want to make multiple modifications to a color such as lightening it and increasing the saturation. Or transparentizing it and darkening it at the same time. And this can be achieved by putting functions inside of other functions.

Let's lighten and saturate a color at the same time:

You maybe thinking that the designs that you work with, or maybe even the designs that you create, are much stricter about their colors than letting them be arbitrarily darkened or lightened or saturated or desaturated within the code, and that's the third point. But there are some occasions when modifying a color is much quicker and much more flexible than endlessly using an eyedropper tool in your favorite graphics package.

By coming up with a system of colors, where a base is tweaked a little bit lighter or darker or more saturated or less saturated, can help us work in this component driven way. And a great example of this is when working with gradients and borders and drop shadows.

Here is another example:

I've got a button with a solid background color and a bit of padding to give the text inside some breathing room. To give the button a bit more detailing, we could perhaps add a border, and a bit of shine with a gradient and some subtle shadows.

Instead of picking colors out of a design file, let's use Sass to take the base color and modify it slightly.

To make this code even more flexible and allow us to generate all sorts of different colored buttons, we can turn our button class into a button mixin, which accepts a parameter for the base color that's gonna be used. Now this mixin can be used to generate buttons of all different colors by including them as needed:

