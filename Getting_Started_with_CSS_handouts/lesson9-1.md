![](headings/BYFW Lesson 9.1.jpg)

# Introduction

Welcome to lesson nine! This lesson's all about **CSS backgrounds**. 

The CSS `background` property allows us to apply background color and background images to any element. This is a very powerful and useful property, because it's used in almost all modern web design. In this lesson, we're going to take a look at some of the basic background properties, including `background-image`, `background-repeat`, `background-position`, `background-attachment`, `background-color`, and the short hand `background` property. Let's start by looking at the `background-image` property.

# Background-image

The `background-image` property allows us to apply one or more background images to an element. We can use a URL value, or one of the keywords, like `none` or `inherit`. The `none` value means that no background image will be applied. This is the default, or the initial value. The `inherit` value allows us to inherit properties from the parent element.

However, the most important is the URL value that allows us to define a path from the CSS file to an image that is applied as a background to the relevant element. The URL path can be relative or absolute.

Here is an example of a relative URL

```
a.png
```

This assumes that the image is in the same folder or same location as the stylesheet.

```
../img/a.png.
```

This is assuming the CSS file has to go up one level and then looking for a folder called *img* and then looking inside that for *a.png* file.

However, a more stable way might be to use relative paths that are root based.

```
/assets/img/a.png
```

It's saying to CSS file: it doesn't matter where you sit, go to the very root of the site and then look for a folder called *assets* and then *img* and inside that look for *a.png* file.

The second method is to use an absolute path:

```
http://site.com/img/a.png
```

# Exercise

We're going to be focusing on the `div.example01` and add a background image to it.

```css
.example01 { background-image: url(a.jpg); }
```

Because this image is positioned in the same place as the stylesheet, we can simply write `a.jpg`.