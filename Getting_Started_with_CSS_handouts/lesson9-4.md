![](headings/BYFW Lesson 9.4.jpg)

# Background-attachment

Let's look at `background-attachment` property.

This property determines whether a background image is fixed or scrolls with the rest of the page. In CSS 2.1, the possible values are 

- `scroll` - the background image scrolls along with the element,and this is the initial or the default value.
- `fixed` - the background image is fixed in relation to the viewport. So even though the image itself might scroll off the page, the background image will stay in place.
- `inherit` - inherits the property from its parent element.

# Exercise

Let's do a quick exercise on the `background-attachment property`. The page has a large amount of content - I've done this for demonstration purposes only.

At the moment, the background image is already in place and it's attached to the body element. If you scroll, you will see that it's actually moving with the page - that's the default behavior. Let's change it:

```css
body { background-attachment: fixed; }
```

Now as you start scrolling, you'll notice that the background image is fixed within the `body` element, and so, it doesn't move with the rest of the page.