There aren't many options when it comes to the letter Z. So we're revisiting a classic, `z-index`. We could have talked about the Sass `zip` function, which combines lists into multi dimensional lists, but I've never really found much practical use for it. However, managing z-index across a project is a much more common concern, and something we can definitely leverage Sass for.

So in this video, we're gonna look at organising layers with Sass map variables, and creating a function to reference layers by name. As discussed in the z-index episode, in the first AtoZ CSS course, having a system for z-index can be useful to bring order, and consistency to your code.

I mentioned in that video that I like to use increments of 10 or 100 for creating different z-index values. So it is more organized than picking random values like z-index 57, or z-index 99999. Using increments of 10, means that you can create different layers at z-index, 0, 10, 20, 30, and so on.

And if you suddenly need to slot in a new layer between two existing ones, you could then pick multiples of 5, 5, 15, 25, and so on. This keeps the code organized, but it's also flexible, and maintainable. To further improve our code organisation, we can use Sass map variables to create a series of layers.

So I've got a demo set up here, with three different coloured boxes, positioned on top of each other. At the moment, the stacking order is determined by the HTML source order as there's no z-index values that have been set. In the Sass, let's first create a variable called layers, which will be a map variable.

For more information on map variables, check out the previous episode on working with Sass maps. This variable allows us to reference our layers by number, and then behind the scenes, output a z-index value with a multiple of 10. We could extend this variable to contain other named values instead of just a numbered series of layers, which could really be useful if you know that there would be certain elements that you want to use in various different layers throughout a project.

I often like to, had a behind layer which uses negative z-index. And then layers for headers, and for models, if this will be ever be used. Having all of the layers abstracted away into a variable like this, means to change, or adjust z-index values throughout the development process, doesn't require changing lots of values across your partials.

We can just modify this z-index values in our variable instead. So, with this variable created how would we use it? In this example, we have three boxes, and if I wanted to change the stacking order, we could do something like this. By using the Sass map-get method, we can fetch the value from the layers variable by its key.

So for box1, we go to the layers variable, and ask for key 3, which will output z-index 30. This works really well, but typing out map-get, and layers all the time, might get a little bit tedious, and we can do better by creating ourselves a custom function. Instead of this repetition in our Sass, we can create a Sass function to output the z-index for us.

We can then, also ensure, that we handle any errors that might occur from referencing invalid layer names, and warn the user accordingly, as we saw in the warn error and debug episode. To clean up this code, first let's define the function. We'll call it layer, and we'll have it accept one argument, which is the name of the layer that we want to output.

Within the function, we then simply return the value from map-get. Having created this function, we can then update our Sass to use it. Instead of manually calling map-get, we substitute that for the layers function, and parse in the name of the layer that we want. So box1, layer(3);, box2, layer(1);, box3, layer(2);.

To make this function even more useful, we can add in some conditional logic, and some error handling. If I call the layer function with a layer name that doesn't exist, Sass doesn't output the invalid value, but it fails silently, which isn't very useful. Let's modify the function to throw an error, if we pass in an unknown layer name.

First we check that the layer name exists by using the Sass map-has-key method. This returns true or false, depending on whether that key exists in the map. If the map does have the layer name, then we'll return the corresponding value, otherwise, we'll use the error directive to alert the user.

We can even use some string interpolation here to output the name of the layer that we specified, and a list of the available keys in the map. This would be useful to let the user know that they just made a simple typo, or try to use a non-existent layer name.

While the system of z-index management is certainly more complex than just plucking a random number out of thin air, having an organized and programmatic approach to authoring a code is a great way to keep your mind organized, and to keep your code maintainable. Sass is the perfect partner for helping you achieve this with minimal effort.

As Sass is a third party tool, and it's not native CSS. It's possible that one day, Sass will be replaced with another tool, or that its functionality eventually winds its way up, as being native to the CSS language. Whatever happens, learning to think like a programmer, and solve problems in a systematic way, will definitely stand you in good stead for your future career.

