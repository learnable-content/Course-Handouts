![](headings/BYFW Lesson 4.2.jpg)

# Why Inheritance Helpful?

Inheritance is designed to make it easy for all of us. Otherwise, we'd need to style all descendants as well as their ancestors. That would mean that our CSS files would be much larger in size. They'd be harder to create and also, much harder to maintain.

Many CSS properties however are not inherited. If every CSS property was inherited, it would make things much harder for authors. As a quick example, what if we start our paragraph element with a border? In this case, a border of `1px solid red`. If the `border` property was inherited, both the emphasis element and the paragraph element would have a border around them. And even worse, we'd then need to turn that off for the emphasis element.

Luckily the border property is not inherited. So we don't need to turn borders off for children when they've be applied to parents. Generally speaking, only properties that make our jobs easier are inherited.

# Exercise

Write a simple style inside *styles.css*:

```css
p { border: 1px solid red }
```

This will put a border around the edge of the paragraph element. Reload the page and note that the emphasis element is not receiving its own border.