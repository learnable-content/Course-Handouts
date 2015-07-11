![](headings/BYFW Lesson 8.3.jpg)

# Floating an Inline Element

Let's look at floating inline elements.

If you might remember from earlier lessons, inline elements are different to block level elements. Width, height, and overflow don't apply, and margin padding and border are applied, but only if it contained on either side of the element. However, when you float an inline element, it becomes a float box. As soon as that happens, width, height, and overflow can be applied. Also, margin pattern and borders will affect content all around the element.

# Exercise

We're going to be focusing on the `strong` element which is an inline element.

```css
.example01 { float: left; }
```

The element will be shifted up off the page and the paragraph will be slid up underneath it; the line boxes will shorten. I just so happens that the second line is just a little bit too short to wrap underneath so that line box gets shortened as well.

The most interesting thing about this element is that it's changed from an inline element to a float box. That means we can give it width, height, borders, etc:

```css
.example01 
{
	float: left; 
	width: 300px;
	border: 30px solid red;
}
```