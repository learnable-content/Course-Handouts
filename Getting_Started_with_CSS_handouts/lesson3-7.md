![](headings/BYFW Lesson 3.7.jpg)

# Introduction

The next topic is **adjacent sibling selectors**. Adjacent sibling selectors are written with a selector that is separated by a plus symbol:

```css
h2 + h3 {}
```

In this example we're looking for any `h3` that comes directly after an `h2` and that they're all siblings, meaning they come from the same parent.

The adjacent sibling selector is not supported by IE6.

# Exercise

We will style an `h4` that comes directly after an `h3`:

```css
h3 + h4 { margin-top: 2em; }
```

We could have assigned that `h4` some class, but this solution seems to be more elegant. We are looking for any `h4`, but only one that comes after, directly after `h3` and that both have the same parent.