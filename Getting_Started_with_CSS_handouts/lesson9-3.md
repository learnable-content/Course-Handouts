![](headings/BYFW Lesson 9.3.jpg)

# Introduction

Next let's look at `background-position` property.

As we saw before, by default, background images are placed in the top left corner of the padding box within the HTML elements. We can change this default positioning using the `background-position` property. In CSS 2.1, two values are used to determine the position of the background image: the first value represents the horizontal axis, and the second value represents the vertical axis of the background image.

We can use length values, percentage values, or even keywords to find these horizontal and vertical axes. These values can be mixed and matched as you need.

Horizontal keywords include

- `left` - will put the left edge of the image to the very left edgeof the padding box.
- `center` - will put the center of the image in the center of the padded box.
- `right` - will push the right edge of the image to the very right edge of the padded box.

Vertical keywords include

- `top` - will put the top of the image at the very top of the padding box.
- `center` - will put the center of the image in the center of the padding box.
- `bottom` - will put the bottom edge of the image in the bottom corner of the padded box.

In CSS 2.1, the length values can include em, ex, px, inches, centimeters, millimeters, points, and even picas. If we're using lengths or percentage values, these values are taken from the top left corner of the element.

We can set positive or negative values to determine the position of background images. A positive value will move the background image to the right and down, or into the background area of the element. Negative values will move the background image to the left and up or out of the background area of the element.

# Exercise

For this exercise we have six different containers. We're going to set them with different positions.

```css
.example01 { background-position: 0 0; }
```

This is the default value so you won't see any difference on the page.

```css
.example02 { background-position: left top; }
```

That's not going to change anything because image is already sitting in the top left corner of that container.

```css
.example03 { background-position: center center; }
.example04 { background-position: right bottom; }
```

This will make the image centered in the middle of that container and place it in the bottom right corner of our container respectively.

```css
.example05 { background-position: 40px 100px; }
```

Keep in mind that we're basing this values on the top left cornero f the container, and the top left corner of the image. So the top left corner of the image will move 40px across, and then 100px down.

```css
.example06 { background-position: 50% 50%; }
```

You'll see that the image here is also centered, like using `center center`.