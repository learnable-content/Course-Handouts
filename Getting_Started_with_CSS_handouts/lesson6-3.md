![](headings/BYFW Lesson 6.3.jpg)

# Inline-block

Now let's look at **inline-block elements**. They appear within lines of text, sort of like inline elements.

By default, the width of inline block elements will collapse, but it can be sized or stretched.

Height of inline-block elements is also collapsed. We can size, but cannot stretch it.

Margin, padding and border can be applied to all sides of the line block elements.

Overflow can be applied to inline-block elements.

Let's talk about the fundamental differences between block, inline, and inline-block.

* With block level elements displayed as blocks, they can be given width and a height. Margin, padding, and border have fixed content on all sides of the element and they can be given overflow.
* Inline elements are the exact opposite. They're distributing lines, they cannot be given a width or height or overflow and margin padding and border only affect the left and right.
* Inline-block is sort of like the best of both worlds, they are displayed as inline elements but they can be given width, height and overflow, and margin, padding and border effect elements on all sides.

# Exercise

Let's style some inline-block elements.

```css
.test01 { width: 200px; }
.test02 { height: 60px; }
```

Width and height will be set for the elements.

So inline-block operates differently..

```css
.test03 { margin: 2em; }.
.test04 { padding: 2em; }
.test05 { border: 1em solid red;}
```

Margin, padding and border will have an impact on all sides of the element.

```css
.text06 { overflow: visible; }
.test07 { overflow: hidden; }
.test08 { overflow: scroll; }
.test09 { overflow: auto; }
```

Overflow will operate just like for block elements.