![](headers/4-2.jpg)
# What we'll be building

Our template includes header, "Our Services" section, "Team" section and footer that includes contact information and locations.

# Getting Started

Let me introduce you a new feature - the `@import` directive that we're using to import external resources: libraries, custom mixins and variables.

Open *libraries/grid.less* file. You will see a bunch of mixins there. There is another file *libraries/elements.less* that we will use as well. In the *custom* folder I've included two files with additional mixins and variables.

Now we will have to use import to load all these files into our project.

# Styling Header section

This is how I import my mixins:

```less
@import "libraries/elements.less";
@import "libraries/grid.less";
@import "custom/variables.less";
@import "custom/mixins.less";
```

Now style the header:

```less
header {
  background: url("../images/background/skyline_ny.jpg");
  background-size: cover;
  height: 500px;
}
```

*images* is the directory with all my images. So right now we're using *images/background*, then the name of the asset. So you may certainly have a path which is much longer. Then you may need to use this path multiple times in your project, if this is a long project. Luckily, with Less, we can use one feature which allows us again to write less code, and this is what we call **string interpolation**. With string interpolation, you can define a variable to which you're going to assign a string value, which can be a URL or a path. Then to refer to this variable, you're going to use the construct that starts with the @ symbol. Then within curly brackets, you're going to use the variable:

```less
header {
  background: url("@{bg}skyline_ny.jpg");
  background-size: cover;
  height: 500px;
}
```

The `@bg` variable is defined as

```less
@bg: "../images/background/";
```

and I simply interpolate its value.

Now proceed with the header section:

```less
header {
  background: url("@{bg}skyline_ny.jpg");
  background-size: cover;
  height: 500px;
	#banner {
		color:@light;
		padding-top: @padding+100;
		h1 {
	  	font-size: @fontSize*2.5;
	  	padding: @padding+30;
	  	display: inline-block;
	  	float: right;
	  	text-align: right;
	  	.text-shadow;
	  	.bordered(xxx, xxx, @light, xxx);
		}
	}  
}
```

I am using a bunch of mixins I've imported previously.