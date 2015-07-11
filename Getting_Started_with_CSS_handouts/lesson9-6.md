![](headings/BYFW Lesson 9.6.jpg)

# Background

Lastly, let's look at the shorthand `background` property.

All of background properties that we looked at can be combined into a shorthand `background` property that defines the URL, the position, the repeat value, whether it's fixed or scrolled, and the background color.

In CSS 2.1, shorthand values can be written in any order. The other thing to note is you don't need to define all these values. You can use one or two, or as many as you want. One thing to keep in mind, is even though you only declare one or more values, for any that you don't declare, an initial value will be used.

# Exercise

For this last exercise we are just going to be changin ga series of background properties into one shorthand `background` property:

```css
.example01
{
	background: url(a.jpg) repeat-x 0 50% yellow;
}
```

As you see the values are separated by a space, but with no commas or semi-colons between them.