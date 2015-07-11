![](headings/BYFW Lesson 10.1.jpg)

# Introduction

Welcome to lesson ten our final lesson! We're going to be focusing on **print CSS**.

Before looking at setting up print CSS files, we need to understand media types.

# Media Types

There are ten different **media types** defined in CSS 2.1:

- All
- Aural
- Braille
- Embossed
- Handheld
- Print
- Projection
- Screen
- TTY
- TV

Before you get worried about all these different types, we really only need to focus on three of them, because most are not supported by browsers at all. So we will focus on all (that means that the CSS file will be used by all types of devices), print (used for print material), screen (means any type of device that supports a screen). 

Let's look at three common methods that we can use to apply media types to our CSS.

The first method is the **link method**. In order to establish a link between an HTML document and a CSS file we can use the `link` element inside the `head` of an HTML document. Within this `link` element we can define the `media` or which types of devices will use this CSS file.

# Exercise

Let's just add a media type for the stylesheet:

```html
<link href="styles.css" rel="stylesheet" media="screen">
```

Now this CSS file would now be read by any device that supports screen. These devices include desktop machines, handheld devices, tablets etc.