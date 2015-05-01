![](headers/3-6.jpg)
# Introduction

With Less you can perform mathematical calculations directly in your stylesheet sby using the operators. So this is what we're going to discuss in this step.

# Using Operator in Less

What we're going to do is to add some margin for the links, around the content and the image.

```less
nav {
  background: @mediumgrey; 
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

This way I am increasing left and right margin by `20px` using `+` operator.

Now add some padding for the container:

```less
.container {
	margin: @margin;
	padding: @padding+10;
}
```

We increase padding for all the sides of this container by `10px`. Something to note is that we're not using any unit of measurement. Less by default uses pixels as a measurment value.

```less
.container {
	margin: @margin;
	padding: @padding+10;

	p {
		font-size: @fontSize;
		text-align: justify;
	}
}
```

I am also styling the paragraph.

Next the footer:

```less
footer {
  .commonRules;
  padding: 0 @padding+10;
  position: absolute;
  left:0;
  right: 0;
  bottom:0;
}
```

Go ahead and check that in the browser.