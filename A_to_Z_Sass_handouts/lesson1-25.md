Setting up a new project can be a time consuming endeavor. The world of front-end web development these days is much more complex than it used to be. And there are now, a whole load of different tools and different workflows to choose from, to create and manage the development process.

In this video, we're going to discuss some of the features of a front-end development workflow. And then a command line tool which can help you get up and running fast. So what's involved in setting up and working on a new project? It used to be that all you needed was a browser, a text editor, an HTML file, a CSS file, maybe jQuery, and a handful of plugins.

Now we've got package managers like npm and Bower, task runners like Grunt and Gulp, bundlers like Webpack or Browserify. Local servers, automatic reloading, pre processing, post processing, and all sorts of other things to help make your workflow faster and more efficient. While these things certainly do take away a lot of the manual tasks and enable you to automate a large part of your development process.

Setting them up can be time consuming at best, and daunting to the point of not even starting at all and worse. So if you wanna see exactly how to set things up step-by-step, we recently released a course on SitePoint Premium all about responsive web development that uses all of these tools.

Now it's a fantastic course, and I highly recommend checking it out. However, if you're already onboard with the benefits of these tools, but you just cringe at the thought of starting every new project because the prospect of having to set them all up, I have an alternative to show you.

Yeoman is a command line tool that can help you automate the setup of new projects. It was developed by a number of very smart people, and it helps you to generate boiler plate code for modern websites and front-end web applications. Yeoman is built on top of Node.js, and it's installed by npm.

So to follow along with the screen cast or to set it up on your own machine, you'll need to ensure that you've got Node installed first. Once node is installed, open your command line tool of choice, and install Yeoman with this single line command. npm install-g yo. This will install the Yeoman command line tool globally.

That's what the -g flag means, which you can then use by running the yo command. When you run this for the first time, you'll see a command line menu with a handful of different options. Install a generator, find some help or get me out of here. You can navigate this menu using your cursor keys and just hit enter to make your choice.

The Yeoman tool isn't actually very useful on its own, but when combined with other tools called Yeoman's generators, things start to get quite interesting. A Yeoman generator is an npm package that provides a configurable set of templates for creating a new project. You can search the web and discover a whole load of different generators for kick-starting all sorts of different projects.

There's ones is for angular apps, backbone apps, ember apps, react apps, bootstrap sites, foundation sites, foundation emails, WordPress sites, and thousands more. If you're feeling particularly adventurous, you can even create your own based on the exact setup that you like, and the exact work flow that you like to use.

If you head to the Yeoman website, and go to the discovering generators page, you can search for whatever kind of project you want to create. Since this is a Sass series, let's find something sassy. There's a lot of fairly average Sass generators out there, but there's a really good one called front-end-sass.

Which will generate a base project using Sass, grunt, BrowserSync, code linting, image spriting, code minification, and automatically add all your vendor prefixes with all our prefixer. More details about the generator can be found on the generator's GitHub page. To install the generator, we need to install it as a global npm package.

So back in your terminal, run the command npm install -g, for global, generator-front-end-sass. With the generator installed, we can now create ourselves a project folder, and then change directory into that newly created folder. So, I call my project yeoman-sass, and then change directory with the cd command. Within the project folder, we can now run the Yeoman generator to scaffold out all of the necessary files and folders, complete with build tools and auto prefixer.

To run the generator, the command to run is yo front-end-sass. Eventually, the generator will finish, and we can take a look at what it did. Here's the project open in sublime text. We started with an empty folder. But after running the generator, there's a whole load of stuff in here.

Opening up the root project folder, we have a development folder for all of our code, and a node_modules folder for all of the npm packages that the generator has installed. There are also a number of configuration files, these are sometimes called dot files that are used to configure a number of the automated tasks that our newly generated project can perform, to speed up our work flow.

In the development folder, we have a JS folder for all of our JavaScript, and a Sass folder for all of our Sass. The generator has automatically generated a solid folder structure for a well-organized Sass project. We've got a styles.scss file, which would be compiled. And it's made up of a number of partials from the base folder.

These partials only contain a few lines of Sass rather than being overly prescriptive and forcing you to go down a particular path. There are some useful mixins for responsive design, and even a shame.scss for any quick and dirty fixes you might wanna do, and then clean up at a later date.

I find this generator to be a really good balance of giving you just enough for a starting point. Without giving you too much code that you might never use, or maybe not even understand. Not only does this generator provide a really good starting point for organizing your project, it comes with a load of tasks that can be run via the grunt command line tool to speed up and automate your development workflow.

So let's have a look at the grunt file and see what it can do. As we saw in a previous episode about compiling Sass with Grunt and Gulp, Grunt is a task runner that can automate common tasks that need to be run as part of the web development process.

These tasks are configured in a JavaScript file called the Gruntfile.js. In this file, we first load the Grunt plugins and set up some configuration variables that tell Grunt where to find our source code, the development folder, in this case, and where to output any compiled files, to a dist folder, in this case.

We also have a browserSync task which is going to launch a local development server and watch all of your files for changes. And by watch, we mean whenever you save the file. And when that happens it will automatically inject any new styles into the page without you having to reload it manually or it will automatically reload the page if the HTML or JS is updated.

We also have a Sass task, which is gonna compile the sass into CSS. It also generates sourceMaps, which we've talked about in a previous video. So check that out for more information on how useful sourceMaps are. Next, we have a post-css task which is gonna run after the Sass has been compiled.

And, in this case, it's gonna run three post processes. It's adding pixel formats for any rem values, and it will automatically add vendor prefixes based on can i use data, and then minifying the resulting CSS. The result of running these three tasks will be saved to the development/css folder.

Next, we have a handful of tasks that are used to check your code for errors and best practices called linters. And also tasks that generate documentation from blocks of comments in the code. We have a task that compiles files from the development folder to the destination folder, which is what would be deployed as a working version of your project.

There's also tasks for compressing images and generating image sprites, which can help reduce the page wait and speed up your site. Finally, we have a watch task which is going to watch all of the source files for any changes, and then run the appropriate grunt task afterwards. For example, the watch styles task will watch for changes in your Sass files and run the sass and the postcss tasks when any files are saved.

After all of the Grunt tasks have been configured, we then register a series of tasks at the bottom of the file. The first and the most useful task is grunt serve, which will launch browser sync, compile sass, and then watch all of your files for changes. Other tasks have also been registered for testing your code, or generating documentation, or running everything all in one go.

That was a lot to take in. So, how do you use these tasks? Let's demonstrate how we would use this set up in development mode. Back in the command line, make sure you're within the project folder, and then run the grunt serve command. This will run the serve task which we were just looking at which will launch the development server, compile your sass, and then start watching the files for changes.

The browser should automatically open but if not, you can browse to http://localhost:3000, and see you work. I'll open the browser and the code side by side to demonstrate how all of these things work. In the Sass, let's add to the base dials. I'll create a variable and set the background color of the body tag.

And as soon as I save, Grunt is gonna kick in and compile the Sass, and automatically inject the styles into the page without even reloading. If I use some css that needs vendor prefixes, like flexbox, these will automatically be added to the compile styles via auto prefixer. So no need to write any vendor prefixes any more.

This kind of automated development workflow is hugely beneficial. It can really speed up your work, and can save you from doing all sorts of manual repetitive tasks. And there's a lot more you can do with these kind of tools, much more than we can demonstrate in a five to ten minute video.

But hopefully, this has demonstrated the kinds of things that are possible, and you can now go, and explore, and create a development workflow that works for you.

