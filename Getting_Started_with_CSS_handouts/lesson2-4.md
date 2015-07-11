![](headings/BYFW Lesson 2.4.jpg)

# Introduction

From a CSS perspective white spaces are completely ignored, so it doesn't matter if we write our rules in one line, or in a whole series of lines:

```css
h1 { color: red }
h1 {
	color: red
}
```

# CSS comments

You can add **CSS comments** into your CSS files easily:

```css
/* comment */
```

Anything between `/*` and `*/` will be ignored by the browser. Comments are used to explain aspects of CSS for ourselves, or for other people who might be using the CSS file later on.

You can write CSS comments in a single line, but you can also write them across multiple lines.

# Exercise

Let's add some CSS comments. Here is the single line example:

```css
/* heading styles */
```

And this is how you can write multi-line comments:

```css
/* 
paragraph styles 
This will be used to style all paragraphs
*/
```

Comments are really important, especially as sites gets larger and more complicated. What they allow us to do is add notes into our CSS file, so that we can explain to ourselves, but also other people who might be looking in our CSS files what these rules are being applied to.