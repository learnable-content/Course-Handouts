![](headings/7.4.png)

# Lesson 7.4 - Static Members

The last thing we're going to talk about with regards to classes is static members. Static members allow you to create methods on a class that are not bound to any instance of the class. Let's look at a `Rectangle` class for instance:

```js
class Rectangle {
  constructor(width, length) {
    this.width = width
    this.length = length
  }

  static square(width) {
    return new Rectangle(width, width)
  };
}
```

That's interesting! Let's see this in action!

```bash
> var square = Rectangle.square(10)
> square.width
-> 10
> square.length
-> 10
```

As you can see, we were able to call the `square` method on the `Rectangle` class without creating a new instance of it. This is useful for situtations like we showed above, and also just for wrapping up code that is relevant to a specific class, but doesn't rely on any instance properties of the class to be useful.