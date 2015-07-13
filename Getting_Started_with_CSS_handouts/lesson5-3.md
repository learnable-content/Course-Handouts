![](headings/BYFW_Lesson_5.3.jpg)

# Order Specified

What happens if the selectors have the same specificity? The declaration that appears last in document order will win.

```css
.intro h2 { color: blue }
h2.new { color: lime }
```