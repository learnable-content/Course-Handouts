![](headings/BYFW Lesson 1.5.jpg)

# Introduction

The third method is to link to external stylesheets.

```html
<head>
	<link rel="stylesheet" href="a.css">
</head>
```

In this case we have a `link` element, the relationship is `stylesheet`. The `href` tells us where to go to reference that stylesheet. In this case it's looking for a stylesheet called `a.css`. 

We can also use the `@import` method.

```html
<head>
	<style>
		@import "a.css";
	</style>
</head>
```

The `link` method is the preferred method for referencing external style sheets, because the `@import` method is often quite slow.

# Exercise

Open up the CSS file with a rule

```css
h2 {color: green}
```

We're going to look in more detail about how to write CSS rules in the next lesson. For now, all we need to know is that any `h2` is going to be green.

But how do we apply that to an HTML file? What we need to do is to link this HTML file to this CSS file:

```html
<link href="styles.css" rel="stylesheet">
```

The first attribute is the `href`, and this will allow us to point to the location of our CSS file. In this case, our CSS file is in the same folder, so we can just use the file name, but if it was in a different location, we may need to use relative or absolute path.

The second attribute is the `rel` (relationship attribute) that tells what sort of file we're linking to.

Reload the page and observe the results!