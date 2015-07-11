![](headings/BYFW Lesson 3.6.jpg)

# Introduction

Now we are going to talk about **child selectors**. Child selectors are written with two selectors that are separated with a greater than symbol:

```css
div > a {}
```

Once again, we start reading from the right. This rule will look for any `a` element, but only one that has a direct child of the `div`.

So with this layout

```html
<div><a href="#">Text</a></div>

<div><p><a href="#">Text</a></p></div>
```

that rule is going to select only the first link, because the second one is not the direct child of `div`.

The child selector is not supported by IE 6.

# Exercise

We're going to target the `a` element inside the `nav`:

```css
.nav li > a { text-decoration: none; }
```