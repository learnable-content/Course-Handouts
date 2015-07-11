![](headings/BYFW Lesson 9.2.jpg)

# Introduction

Now let's have a look at `background-repeat`. We're going to start with a quick look at three different types of boxes that are relevant to backgrounds.

- **Content box** is the box that houses all the content inside an element.
- **Padding box** is only relevant if the element has been given padding.
- **Border box**.

By default, background images are set to repeat along both the X and Y axis. The image is set to start from the top left corner of the padding box. Even though they start from the top left corner of the padding box, they can repeat outwards in all directions, including the border box area.

In CSS 2.1 we can change the repeat behavior using four different key words:

- `repeat` - will repeat the image that are crossed by the X and Y axis andwill cover the entire background image of that element, including the padding andborder boxes.Now this is the initial or the default value.
- `repeat-x` - will repeat the background image only along the X axis.
- `repeat-y` - will repeat the background image along the Y axis.
- `no-repeat` - will set the image not to repeat at all.

# Exercise

We are going to work with four containers that already have a background image in place. We will change the `background-repeat` values in each of these four boxes.

```css
.example01 { background-repeat: repeat; }
```

That's the default value and won't visually change anything.

```css
.example02 { background-repeat: no-repeat; }
```

The background image won't be repeating anymore.

```css
.example03 { background-repeat: repeat-x; }
.example04 { background-repeat: repeat-y; }
```

In this case background image will be repeated only on the X and Y axis respectively.