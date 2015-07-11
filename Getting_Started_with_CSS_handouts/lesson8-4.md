![](headings/BYFW Lesson 8.4.jpg)

# Clearing Floats

Now let's talk about **clearing floats**. If you don't want elements to interact with floated items above, you can force them to clear or sit below these floated items using one of three `clear` property values.

You may use `left`, `right` or `both` if you want an element to sit below left-floated, right-floated or floated to any side element respectively.

# Exercise

First of all, set floating:

```css
.float01 { float: left; }
.float02 { float: right; }
```

What happens if we want to clear all of the paragraphs?

```css
.clear01 { clear: left; }
```

The paragraph will moved out or cleared the left-floated element.

```css
.clear02 { clear: right; }
```

This paragraph has now cleared the right-floated element.

```css
.clear03 { clear: both; }
```

This last paragraph is clearing the left- and the right-floated element.

