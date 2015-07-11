![](headings/BYFW Lesson 4.1.jpg)

# CSS Inheritance

Welcome to lesson four! This lesson is all about **CSS inheritance**.

Inheritance is where CSS properties are passed down from paired elements to descended elements.

```html
<body>
	<p><em>Text</em></p>
</body>
```

What is going to happen if we write the following rule for this example:

```css
p {color: red}
```

The paragraph and the emphasis element are both going to be colored red. But why is the emphasis element colored red, when it hasn't been given any style of its own? This element is a child and it has inherited the `color` property from the `p` element.

# Exercise

Write a simple rule inside *styles.css*:

```css
p {color: red}
```

If you reload the page, you will notice that the paragraph and the `em` element are both colored red.