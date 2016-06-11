![](headings/7.1.png)

# Lesson 7.1 - Introducing Classes

A great feature in ES2015 is the brand new `class` keyword. Classes are not baked into ES2015, but rather, are just some syntactic sugar over a pattern that is well established in the JavaScript community.

This pattern is the prototype chain. Every object in JavaScript has an object called the prototype. You can add functionality to the prototype of any object that you would like, and JavaScript developers have been doing this for years. So you can create something like a class like this:

```js
var Foo = function(x) {
  this.x = x
}

Foo.prototype = {
  add: function(y) {
    return this.x + y
  }
}
```

Adding the `add` function to the prototype will give every instance of `Foo` the `add` function.

## Classes!

This exact same pattern can be expressed like this using ES2015:

```js
class Foo {
  constructor(x) {
    this.x = x
  }

  add(y) {
    return this.x + y
  }
}
```

This is a nicer looking syntax, but doesn't offer anything extra in the way of functionality. It simply gives us a much nicer way to implement classes and class inheritance like other programming languages that already have this functionality.