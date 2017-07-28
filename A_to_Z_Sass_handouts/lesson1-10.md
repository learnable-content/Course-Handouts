Having embraced the power of Sass and started to use variables to configure various settings and styles in your projects, Such as colors, font sizes and media query break points, you might start to wonder how you can share these values between other front end languages such as JavaScript.

In programming, we often want to minimize duplication, and declaring variables in both your Sass files and your JavaScript files would be a maintenance nightmare. There are a couple of ways to share data between Sass and JS using JSON. In this episode, we're gonna cover the theory rather than too much of the practice, to keep things brief and to not end up going down a huge, deep JavaScript rabbit hole.

But in this video, you'll learn about the similarities between Sass map variables and JSON. How to convert Sass into JSON and read it in JavaScript. How to convert JSON into Sass, and a number of resources and tools to help with the conversion process. In this series so far, we've not really spent too much time looking at Sass map variables as we've got a whole video coming up very shortly.

However, Sass maps and JSON serve a very similar purpose and have quite a similar syntax. They're both stores of key and value pairs that can hold also to different types of values, each with a unique key or label. Here's a comparison of the two with the Sass on the left and the JSON on the right.

As the syntax of both these data types is quite similar, it's possible to convert a Sass map into JSON or JSON into a Sass map. Before looking into how this can be done and some tools to help us get there, let's first have a think about why we might wanna do this.

Every project is different but there are some common use cases for sharing data between languages. So you might want to share colors or switching between different visual themes, we might wanna share breakpoint values for detecting screen sizes in JavaScript, We might wanna share breakpoint values for working with responsive image solutions.

We might want to share version information or other sorts of meta data across the different languages as well. So let's start by looking at how Sass can be converted into JSON, and then made available in our JS files. Styling information should be kept in Sass or CSS as much as possible.

So starting with a Sass variable and converting it into JSON seems like a good, logical first approach. The idea is to convert the Sass map into a JSON string using some kind of tool, And then apply it to the content property of a pseudo element so that it can be selected and read by JavaScript.

A good choice is the body before element as it's rarely use for any other visual purpose. So after processing our Sass into JSON, our compiled CSS might look something like this. This content value can then be read by JavaScript using the getComputedStyle method and sanitized and then passed into JSON.

I won't go through all this code in too much detail but here is one approach that you could use for doing those two tasks. Having gone through this somewhat long winded process, your Sass variables would now be available in JavaScript, And could be accessed through the sassVars JavaScript variable.

So for example, to fetch the color blue out of our Sass files, we could call sassVars.colours.blue, and then log that to the console or do whatever else we wanted to do with it. An alternative and slightly simpler approach is to start with a JSON file that contains all of the shared variable information.

Using a third party tool like Sass JSON Vars, the JSON file can then be imported into your Sass file directly. This technique leverages the confusing power of a more powerful language to do the conversion, rather than leaning on Sass to pass all of it's native map variables into a JSON string.

And because JSON is easily consumed by JavaScript, there's very little work to be done on that side of things other than to load the file. There's no extra passing or sanitization requirement. If I have a need to share data between the two languages, between Sass and JavaScript, this is definitely the approach that I would used for sure.

It just seems a lot simpler. So let's take a look at some of the other conversion tools that can help make this happen. When researching this topic, I came across a number of blog posts and a number of different tools to help convert Sass to JSON and vice versa.

This is a relatively advance topic but it seems that the desire to share this information between the different languages is really, really strong. To aid in converting Sass maps to JSON, you can check out SassyJSON, which is a pure Sass solution that converts Sass maps into JSON and was written by Hugo Giraudel.

There is also Sass to JS which is another Sass tool that converts Sass to JSON, But it also bundles JavaScript helpers to aid in reading them from your CSS into JavaScript. To go the other way around and to start with the JSON file and convert it into Sass, there is Sass JSON Vars which we've already discussed.

This is a ruby gem which allows you to directly import a JSON file with the Sass at import command. There's an alternative version if you are using node-sass with something like gulp for combining your styles. Also found another gulp plugin called gulp-json-sass, which converts a JSON file into a Sass file with the series of global variables.

So whether or not you have the need to share variables between your Sass and your JavaScript, I hope this trip down the Sass rabbit hole has demonstrated just how much power we have at our fingertips when using this fantastic tool.

