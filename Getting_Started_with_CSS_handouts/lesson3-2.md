![](headings/BYFW Lesson 3.2.jpg)

# Introduction

Now let's discuss **class selectors**. Class selector is written with a full stop followed by the class name value:

```css
.intro {color: red}
```

It's important to remember that CSS class names are case sensitive, so the two examples below would be treated differently by browsers:

```css
.intro {}
.INTRO {}
```

Class selectors are well supported across all modern browsers.

# Exercise

Let's style our container. The selector would be "dot" for class and then "container":

```css
.container
{
	width: 50em;
	margin-left: auto;
	margin-right: auto;
}
```

By setting the `margin-left` and `margin-right` to `auto`, we are centering the container in the viewport.

Now style another class:

```css
.nav
{
	padding: 1em 2em;
	background: green;
}
```

Now our `.nav` element has some padding and a green background.

Now for another class:

```css
.intro
{
	font-size: 1.2em;
	color: gray;
}
```