![](headings/BYFW Lesson 3.4.jpg)

# Introduction

Now let's talk about the **universal selector**. The universal selector is just written with a star:

```css
* {color: red}
```

This would select the `head` element and any children of the `head`, as well as the `body` element and any children of the `body` element. So basically it gets every element on the page.

The universal selector is well supported across all modern browsers.

# Exercise

Let's do a quick exercise:

```css
*
{
	margin: 0;
	padding: 0;
}
```

This can have a radical effect on the layout. Some people do use this to do what's called zeroing margins and paddings of all elements. In our case however it's a little bit too dangerous and would involve a lot of extra work so comment out that rule.

So, the universal selector is actually very powerful and can have some radical effects of the page, so you've got to be careful to use it wisely.