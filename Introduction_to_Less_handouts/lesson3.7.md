![](headers/3-7.jpg)
# Introduction

In this step we're going to talk about built-in Less functions. With Less, it is possible to run functions in order to access existing information that we have on the page. So to put it more simply, what we're going to do is create new colors from existing colors that we have on the page.

# Built in functions

There is the function `lighten` which increases the lightness of a color. It accepts the color and the amount by how much you want to increase the lightness. This can be any value between zero and  100%.

You also use the function `darken`, that does the opposite by decreasing the lightness of an existing color.

You can find the full list of the built-in functions supported by Less by going to [lesscss.org](http://lesscss.org) and Functions section.

# Function Demonstration

I'm going to start by defining a new variable:

```less
@template_color: @wisteria;
```

It uses the existing variable which is assigned with hex code color. What I'm aiming for is to create a new design by creating new colors from an existing color. This way we're going to have a design with different shades of an original color.

Update `@border` like this:

```less
@border: 4px solid darken(@template_color, 5%);
```

Now update the `commonRules` mixin in the same way:

```less
.commonRules {
	padding: @padding;
	margin: 0;
	color: lighten(@template_color, 45%); 
	background: @template_color;
	text-align: right;
	.bordered;
}
```

Check out the output in CSS.

Continue with the navigation:

```less
nav {
  background: lighten(@template_color, 10%);
  ul {
  	margin: 0;
  	li {
			display: inline-block;
			font-size: @fontSize;
			margin: @margin @margin+20;
			a {
				text-decoration: none;
				color: @lightgrey;
			}
		}
  }
}
```

What you can do next is redefine your `@template_color` variable:

```less
@template_color: @green_sea;
```

This way you have entirely different colors and to achieve that you've performed only one operation. So you can play around with creating new colors from existing ones by using functions like `darken` and `lighten` in order to access different shades of an existing color.