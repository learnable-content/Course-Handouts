![](headings/BYFW Lesson 9.5.jpg)

# Background-color

Let's look at the `background-color` property.

As you'd imagine, the `background-color` property sets the background color of an element. The background of an element is the total size of the element, and that includes the padding box and the border box. 

`background-color` can be defined using a color value or the keywords `transparent` or `inherit`. The `transparent` value sets the background color to transparent or see-through, and this is the initial or the default value. The `inherit` value inherits the property from its parent.

We want to focus on background colors and how we apply them. This can be done in a number of different ways:

- Use a keyword like `red` or `yellow`
- Use a six-integer or three-integer hexadecimal color.
- Use RGB values.
- Use RGBA values which means red, green, blue and alpha. This allows us to set the background color to be semi-transparent.
- Use HSL or HSLA, that stands for hue, saturation, and lightness and alpha.

# Exercise

Let's add some CSS rules to change background color of our containers:

```css
.example01 { background-color: transparent; }
```

That's the default value, so when you reload the page, nothing will visually change.

```css
.example02 { background-color: yellow; }
```

Here we are using a keyword.

```css
.example03 { background-color: #ddd; }
```

Hexadecimal value is used for color in this case. `#ddd` is the soft gray color.

```css
.example04 { background-color: rgba(255,255,0,.5); }
```

Here we are using RGBA to set background color. The last value is the alpha value, which we can set between 1 and 0 (1 being solid and 0 being completely transparent).