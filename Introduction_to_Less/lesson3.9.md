![](headers/3-9.jpg)
# Types of comments

In this step we're going to talk about the **comments**.

The first type of comment that you may have is an **inline** comment, that would fit on one line. You'd use the two forward slashes `// ...` followed by your comment in order to make it invisible.

There is also the **block-style** comment, which is a multi-line comment, that yo uwould insert within forward slash and asterisk `/* ... */` in order to make it invisible.

# Difference between inline and block style comment

This first example, the block style comment with multiple lines, will be visible in the CSS file:

```less
/* 
 * LESS Variables are defined with an @ character
 * and can have different kinds of data types: 
 *  color, string, boolean, multi-value
 */
```

This one will be visible in the Less code, but not in the CSS file:

```less
//Less comment silent - invisible on CSS file
```

So, depending on the purpose of the comment, for example, in a collaborative situation, you can use either an inline or block-style comment. For example, if you want to provide with indications or instructions to other developers working on the Less code, you'd be using inline comments that would be invisible and silent in the CSS output. We can use block-style comment for the purpose of organizing the CSS output. They are going to be visible inside the CSS files.