![](headings/BYFW Lesson 6.2.jpg)

# Inline elements

Now let's look at **inline elements**. Inline elements are distributed in lines. They're not formatted as blocks like block-level elements. By default, the width of inline elements is collapsed and it cannot be sized or stretched. The height of inline elements is collapsed and cannot be sized or stretched.

Margin can be applied to all sides of inline elements, but these margins only affect content on the left and right sides.

Padding can be applied to all sides of an inline element, but it only affects content on the left and right.

Borders can be applied to all sides of inline elements, but only fixed content on the left and right.

Overflow does not apply to inline elements.

We can take a block element and make it inline:

```css
h1 { display: inline }
```

# Exercise

Let's style some inline elements.

Write the first rule:

```css
.test01 { width: 200px; }
```

Because it's an inline element, width won't be change - width does not apply to inline elements.

```css
.test02 { height: 60px; }
```

Once again, this is the inline element therefore this rule is not being applied.

```css
.test03 { margin: 2em; }
```

Unlike block level elements where margin affects everything all around the element, for the inline elements, margin is only affecting content on the left and right - no effect at top and bottom.

```css
.test04 { padding: 2em; }
```

Padding works by pushing the content inwards. Even though padding is being applied to all sides, it's only having an effect on the content to the left and right of the element.

```css
.test05 { border: 1em solid red;}
```

The border is being applied around the element. It has no impact on the content above or below, but it is pushing away the content on the left and right.