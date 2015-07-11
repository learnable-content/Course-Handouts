![](headings/BYFW Lesson 2.3.jpg)

# Introduction

There may be times when you want to write some declarations, but that are relevant to one selector:

```css
h1 {color: red}
h1 {margin: 0}
```

We can combine the declarations within one declaration block:

```css
h1 {
	color: red;
	margin: 0;
}
```

After each declaration we need to include a semicolon. If there are two declarations, and there's no semicolon between them, both of those declarations will be ignored. You can leave off the semicolon at the very last declaration, but it's probably not a good practice in case you want to come along later and add a new declaration.

# Exercise

Let's go and write some multiple declarations.

Inside the *styles.css* we have a range of rules. This time, all the properties and values are different, but the selector is the same. So let's optimize it:

```css
p {
	background: yellow;
	padding: 20px;
	margin-top: 20px;
	margin-bottom: 40px;
}
```