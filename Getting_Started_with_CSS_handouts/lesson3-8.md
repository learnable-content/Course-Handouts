![](headings/BYFW Lesson 3.8.jpg)

# Link Pseudo-class Selectors

Now let's talk about `:link` pseudo-class. This is written with an element, normally an `a`, followed by colon and then `link`:

```css
a:link {}
```

You cannot have whitespace between the element and the colon or between the colon and the keyword `link`.

Next up, `:visited` pseudo-classes:

```css
a:visited {}
```

What does it do? It's going to look for any link element, but only one that's been clicked on by the user and then determined as visited.

Next up, `:focus` pseudo-class selectors:

```css
a:focus {}
```

This is going to style any element that's currently in focus. That means the user, generally speaking, has tabbed to that element and it's now in focus. This is really important for keyboard users.

Next up, the `:hover` pseudo-classes:

```css
a:hover {}
```

This is going to style any `a` element that's in hover state, that means the user has rolled over that with their mouse and the element is changed to a hover state.

Now the `:active` pseudo-class:

```css
a:active {}
```

`:active` means that the user has interacted with an element. In many cases, this is something like an element that has been clicked on. So just in that point when the user clicks on it, it's considered active.

First thing we're going to do is to style all of our links to a color of green:

```css
a:link { color: green; }
```

Next the visited state of links (the links that have been clicked on by the user):

```css
a:visited { color: brown; }
```

The next state is the focus state:

```css
a:focus { color: black; }
```

Use the same approach so style hover and active states:

```css
a:hover { color: lime; }
a:active { color: red; }
```

# Order Specified

Before we wrap up, a quick discussion on the order that these pseudo-classes should be written in. Some people use the phrase *"love hate"* to remember the order. So "L" for "link", "V" for "visited", "H" for "hover" and "A" for "active". Unfortunately, this one doesn't include focus, so it's not my favorite term.

Another one is *"Lord Vader, Former Handle Anakin"* and that at least gets all the five different states. So we have "Lord" for "link", "Vader" for "visited", "Former" for "focus", "Handle" for "hover" and "Anakin" for active".

Regardless, the quickest way to think about it is the two static states. A link is either link or visited, which means it's unvisited or visited. Those two should always be written first. Then we have the three active states: focus, hover and active. The last thing you're likely to do in a link is click on it and send it in that active state.