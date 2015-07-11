![](headings/BYFW Lesson 1.4.jpg)

# Header Styles

The second method you could use is **header stylesheets**. This is where you put a `style` element in the top of your document and you write a CSS rule inside the HTML document.

```html
<head>
	<style>
		h2 {color: blue}
	</style>
</head>
<body>
	<h2>Text</h2>
</body>
```

In this case, we're setting color of `h2` to blue. This would mean that any `h2` on that page would be colored blue.

Like inline styles, header styles should be avoided generally as they're inefficient and hard to maintain. If you have many web pages, you will have to edit header styles on each page. However, header styles can be useful if you're trying to do a quick test, and you want to write some quick rules in the head of the document, just to see what's going on. But for a real website, this is not a good solution.
