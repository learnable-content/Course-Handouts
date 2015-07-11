![](headings/BYFW Lesson 1.3.jpg)

# Inline Styles

Let's now look at applying CSS to web pages. There are three different ways that we can apply CSS to web pages.

The first way is called **inline styles**.

```html
<h2 style="color: red">Text</h2>
```

In this example you can see we have an `h2` element, and then we're using a `style` with `color: red`. So that's going to style just that `h2` element to be red in color.

Generally speaking, inline styles should be avoided as they're inefficient. You can only apply an inline style to a single element and they're really hard to maintain because if you need to change them across a range of documents, you have to change every single instance.
