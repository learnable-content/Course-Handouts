I'm a big fan of **animations**, I covered them back in our first series of A to Z CSS. And now we're gonna look at the sassy variety too. So in this video we're gonna cover a quick recap of how CSS animations are made. And then a step by step process of creating and refactoring a mixin for working with animations.

Let's start off with a quick recap of how CSS animations work just to refresh your memory and to give ourselves an example to work with. So, most animations change a series of style properties over time by specifying a series of keyframes with a percentage syntax. So for example, we could animate the left position of an element from 0 to 100% and then back again using a snippet a bit like this.

First we have a block of keyframes which describes the key moment in time throughout the duration of the animation. Then we apply those keyframes to an element, or to multiple elements if we wanted to, by setting the shorthand animation property. In this case, this is made up of the animation-name, the aniimation-duration, the animation-direction, the animation-iteration-count, and the animation-timing-function properties.

With this type of animation, we specify the styles for the key points in the animation and then the browser works out all the in between states automatically. So hopefully that's been a useful if not a brief refresher of animations. The key point here is that the keyframes and the animation properties work hand in hand.

And since that's the case, we could use a little bit of Sass to clean up our code a bit by using a mixin. So let's walk through a staged example to build out that mixin and then refactor it as we go to make it as flexible as possible.

So let's continue with the example that we've just been looking at, so that we've got a bit of context and so we don't have to write too much more code. Since we want to create and use the keyframes at the same time, we could create a mixin that takes arguments for each of the various animation properties.

And then use the @content directive so that we can create the keyframes within the body of the mixin. So working in this way provides an interface to create both keyframes and then pass in all various properties that we want to set all at once. And if we wanted to use that mixin, it would look a little bit like this.

So if we refresh the page, we should see that this still works, but there are some limitations here. Firstly, we've got to specify each of the parameters in the mixin when calling it with @include. Or if we wanna skip some of the values, we'd have to pass in a null value.

Secondly, we'd have to remember the correct order for all of these parameters and there's quite a lot of them. And that could potentially be fraught with a lot of human error, and because of the way Sass works, we can do a little bit better. We can do this by specifying default values of null in the mixin definition.

And if we do that for everything other than the name and the duration, so mark the delay, the iteration, the direction, the fill-mode, and the timing all as null. Then we don't have to specify those every time we include the mixin. But this still doesn't solve the problem of needing to remember a correct order for all the parameters which is a bit of a problem.

So instead we can construct our mixin to accept a variable number of arguments. And then use the animation shorthand property to apply them all at once. And we can do this using a special dot dot dot operator which comes after the parameter name in the mixin definition. So we can refactor it like this, we'll keep the name but then instead of all of the other properties which we previously had optional as null.

We'll now create a different variable called properties with this three dots afterwards. Now our mixin takes the first required parameter for the animation name. And then a variable number of properties which can be use with the animation shorthand property. So our mixin declaration is now much shorter and much more flexible, but we can actually take this one step further.

One of our goals as diligent Sass developers is to reduce repetition in our code and to reduce our thinking time wherever possible. So when creating an animation in this way, we're generating the key frames and the animation properties all at the same time. So really we don't need to provide a meaningful name to the animation because Sass takes care of outputting everything for us.

So instead of having to think of a name, which can sometimes be difficult, we could just have Sass generate a unique one for us automatically. Sass has got a built-in feature called the unique ID function, which returns a randomly generated, nine character string of letters and numbers. And it will do this every time the Sass is compiled.

So using this unique reference, we can actually remove the name parameter from the mixin declaration and just save the unique ID into a variable. This variable can then be used with interpolation, like we looked at in a previous video, to create a single animation shorthand comprised of the name and/or the other properties in a single line.

So we've hugely improved the manual way of outputting animations, however, there is a downside to this method. If you wanted to create a series of keyframes that would be reused multiple times by different selectors, say for example with different values of animation delay. Then using this mixin it is impossible because the name of the animation has been abstracted away.

I'd probably argue that we've refactored it just one step too far and actually made it overly complex. And maybe a little too abstract, and not suitable for creating reusable animations. While we've learned a couple of advanced Sass tricks here, which is always fun, I'd probably revert this code back to the previous iteration of the mixin.

So passing in the name and then the series of animation properties. That way the mixin is still pretty lean, but it's also a bit more meaningful and it's flexible if we wanted to re-use our key frames elsewhere.

