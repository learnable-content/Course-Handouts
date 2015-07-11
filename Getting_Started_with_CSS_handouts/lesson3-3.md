![](headings/BYFW Lesson 3.3.jpg)

# Introduction

In this step we will discuss **ID selector**. The ID selector is written with a hash symbol followed by the ID name:

```css
#sidebar {color: red}
```

Just like class names, ID names are case sensitive.

One thing for you to keep in mind is that you can only have one instance of the ID on a page.

The ID selectors will supported across all modern browsers.

# Exercise

Let's style the header and footer:

```css
#header, #footer
{
	padding: 2em;
	color: #fff;
	background: #000;
}
```

Now style an element with an ID of `main`:

```css
#main { margin: 1em 2em; }
```

That's going to put a margin of `1em` on the top and bottom, and `2em` on the sides.

What's the difference between margin and padding? Padding affects content on the inside of the element. If you put padding on an element, that will push content further into the middle of that element.

Margin, on the other hand, will affect things on the outside of the element. It'll push things up or down, away from that element.