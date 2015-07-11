# Introduction

We can use inheritance to write efficient CSS. For example, you can set the `font-size` and `font-family` on the `body` element, and then these properties will be inherited by all descendant elements. On a lower level you can override those properties as needed.

# Exercise

Open up *styles.css* file. Start by writing a rule for the `body` element:

```css
body
{
	font-family: arial, helvetica, sans-serif;
	font-size: 90%;
}
```

What if we wanted all of our headings to be in a serif font? We can do that writing the following rule:

```css
h1, h2, h3, h4, h5, h6 { font-family: georgia, times, serif; }
```

You should see that the headings have now changed to either Georgia, or Times, or at least some sort of sans-serif font.

The last thing that we're going to do is set the `h1` to a larger size:

```css
h1 { font-size: 220%; }
```