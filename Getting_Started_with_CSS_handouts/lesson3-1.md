![](headings/BYFW Lesson 3.1.jpg)

# Introduction

Welcome to lesson three! This lesson's all about **CSS selectors**. Selectors are very important as they allow you to target specific HTML elements to be styled.

The selector selects the HTML elements on an HTML page. There are 57 different selectors that can be used in CSS. We're going to cover 12 of the most important selectors in this lesson.

# Type Selector

The **type selector** is written with an element:

```css
h1 { color: red }
```

Here we style all `h1` on a page.

The type selector is well supported across all modern browsers.

# Exercise

Open HTML and CSS files for this lesson. We'll be working through a series of exercises to use selectors in order to style this page.

First of all, let's style the `body`:

```css
body
{
	margin: 0;
	padding: 0;
	font-family: arial, helvetica, sans-serif;
}
```

By default most browsers have a bit of margin and padding around the edge of the page and we just get rid of it. We're also setting the font family.

Now let's style some headings:

```css
h1 { margin: 0; }
h2,h3,h4,h5,h6 { color: green; }
```

By default, most headings have a bit of margin above and below, so we get rid of them. Next set color to green.