![](headings/BYFW Lesson 2.2.jpg)

# Introduction

There may be times when you want to apply some styles to many elements. You could write

```css
h1 {color: red}
h2 {color: red}
h3 {color: red}
```

But that's not very efficient. Use multiple selector instead:

```css
h1, h2, h3 {color: red}
```
 

There is one catch however. You can write a series of selector and they can all be separated with a comma but you cannot have a comma after the last selector. If you do, the entire rule will be ignored.

# Exercise

Open up the *styles.css* file that has some styles already defined. There are a bunch of different selectors, styling `h1` through to `h6`, however, they all have exactly the same declaration applied. So we could write that much more efficiently:

```css
h1,h2,h3,h4,h5,h6 { border: 1px solid red; }
```
