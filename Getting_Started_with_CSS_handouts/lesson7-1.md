![](headings/BYFW Lesson 7.1.jpg)

# Understanding CSS Positioning

Welcome to lesson seven! This lesson is all about **CSS positioning**.

There are five methods that can be used to position HTML elements:

- static
- absolute
- fixed
- relative
- float

In CSS elements or boxes are defined as being either in normal flow, or out of normal flow.

**In normal flow** is when boxes flow down the page without any positioning implied. An example might be a series of headings or paragraphs that flow down the page. By default, all elements or boxes will be in normal flow. The term "in normal flow" is also referred to as in-flow or static positioning.

**Out of flow** is when a box is given some sort of positioning, and this could be absolute, relative, fixed or float. When a box is given positioning, or floated, it moves up off the page and out of the normal flow.

Let's now look at the first positioning model, which is **static**. Static positioning is a default positioning method. The element will be displayed without any positioning or float being applied, and will be in normal flow. This value doesn't need to be applied in most cases, however, you can apply it to remove the positioning of a box that previously had some sort of positioning. The `top`, `right`, `bottom` and `left` properties do not apply to static positioning.