![](headings/BYFW Lesson 5.2.jpg)

# CSS Specifity Exercise

Let's do a quick exercise. We're going to be focusing on the `h2` element (with a class of `news` and an ID of `intro`) and write a series of rules to see which one will win in setting a color for this element.

The first style to add is

```css
h2 { color: green; }
```

That should set green text color for all the `h2` elements on the page.

Now focus on the specific `h2` element:

```css
.news { color:blue; }
```

The second heading now has blue color. Why did that happen?

Lets look at our first selector. It has no inline styles, no IDs, no classes and one type selector - therefore it has a specificity of 0,0,0,1. However, `news` has a class in its selector. No inline stars, no IDs, one class, no type selectors - therefore it has a much higher specificity of 0,0,1,0.

Our next selector is `h2.news` that is looking for any `h2` element that has a class of `news`:

```css
h2.news { color: orange; }
```

The `h2` is now orange and that's because this selector has a higher specificity. No inline styles, no IDs, but it does have a class and a type selector, so specificity is 0,0,1,1.

The next selector is `#intro`, which is an ID:

```css
#intro { color: purple; }
```

As you'd expect, our heading has now gone purple. No inline styles, but it does have an ID, no classes and no types - therefore this style has a specificity of 0, 1, 0, 0.

Next up we're styling `h2` with an ID of `intro`:

```css
h2#intro { color: aqua; }
```

The heading has now gone aqua, and the specificity for this style is 0 inline styles, 1 ID, 0 classes, but one 1 selector - therefore it has a slightly higher specificity of 0, 1, 0, 1.

Now open up the HTML file and add the following attribute to `h2`:

```html
style="color: red"
```

The heading will now be red. This is because it has the highest of all specificities - it has an inline style.