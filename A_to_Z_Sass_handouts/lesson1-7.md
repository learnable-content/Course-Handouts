In this episode, we're gonna be diving into two more command line tools that can help you compile Sass. Now, they both do a lot more than just compiling Sass, so they're definitely worth looking into. And then you can choose which one you like the look of the best.

But for the purposes of this video, and keeping it short and sweet, we're just gonna focus on the Sass side of things. So in this video, you'll learn what Grunt and Gulp are and why they're useful, how to set up Grunt to compile your Sass. How to set up Gulp to compile your Sass, and then some next steps for supercharging your workflow with either of these two tools.

Grunt and Gulp are two popular tools for helping you automate your development workflow. They're command line tools and they are written in JavaScript. And to use them you need to install NodeJS and the npm package manager, the node package manager. If you wanna follow a long with this video step by step, then do make sure you've go this things installed.

And you can head over to the NodeJS website for installation instructions. Grunt and Gulp can both perform a number of different tasks for jobs like minifying or compressing your code, concatenating multiple files together, checking your code for errors with things like CSS Lint or JS Hint. Or, they can be used for compressing images or compiling Sass.

They both have a slightly different approach to these tasks, and you'll only ever use one or the other on a single project. Tools like this can sometimes sound a little bit complex if you're not familiar with them. And they can be a bit abstract or even a bit scary if you're new to app development.

You're not alone, I felt exactly the same way in the past,. And it took me a long time to actually give one of them a try. But the only way to get better at your craft and to hone your skills is to break out of your comfort zone.

So I really would encourage you to give these a go, or at least, watch the whole video. For a great introduction to tools like Grunt and Gulp, Chris Coyier wrote a fantastic article titled, Grunt for People Who Think Things Like Grunt are Weird and Hard. Which I think sums up the sentiment of a lot of people who are coming to these things for the first time.

So let's dive into a practical example and go through everything step by step to show you how to use both Grunt and Gulp. You can then decide which one you prefer or choose to use neither of them at all and stick with your existing process. So for this Grunt example I've got a simple project here which has got an SCSS folder containing a main.scss file and a CSS folder which is where the styles are gonna be compiled into.

So as long as you've got node and npm installed, the next thing we need to do is to install Grunt. And this is done from the command line with the following command, npm install grunt-cli -g. The -g stands for global, and this will install the grunt command line interface so that it could be used on any of your projects.

Now, this is something that you only do once. If you already got Grunt installed, then you don't need to do this, you can skip this step. Once Grunt has been installed, we need to create another file called package.json. And that's gonna contain information about a series of other tools called node modules that Grunt is gonna need to perform all of the various tasks.

In our case, it's gonna be things like watching the files for changes and compiling Sass. So on the command line, ensure that you're still in the project folder and in the root of the project, and run the command npm init. If you're doing this to set up a real project,then go ahead and fill in all the answers to the various questions.

Or, if you just wanna get up and running quickly, just hit Enter through all of them and it will use the default values. Now that we have initialized a package.json, we can install local version of Grunt and two additional packages, one for watching files for changes and one for compiling our Sass.

So to install these packages, we need to run the following command. If you hit Enter and wait for everything to churn away, eventually you should see a success message. And now if you look in your package.json file, there should be a list of the three packages that we just installed.

With all these dependencies installed, we now need to create a configuration file to tell Grunt what we want it to do. So, if you create a new file called gruntfile.js, all one word, lower case, in the root to the project, then we can add the following code. To save you typing it all out, head to atozsass.com and you can just copy and paste it.

This sets up two Grunt tasks, one of them is called watch that is gonna watch our Sass files for changes. And the other task is called Sass and that's gonna compile our main.sass into main.css. If you use a similar setup like this for future projects, you may just have to make adjustments to the various file paths.

But this should work for the simple example here. Having created the configuration file, we can now run the Grunt command in the terminal, and optionally specify the name of the task that we want to run afterwards. So if we run grunt Sass, it will run the Sass command and our styles will be compiled once.

Running the command grunt watch will run the watch task. And Grunt will keep running in the background and it will just watch for changes to the files. And it will keep watching for changes until you quit by using the keyboard shortcut CTRL+C. A third way of kicking all this off is to just run the Grunt command without any task name and that will run the default task, which in this case, has been configured to run watch.

But it could be configured to do all sorts of other things as well. So to double check that everything is working, open up the main.scss file, write some Sass code in there, hit Save, and check the terminal. And you should see that Grunt has detected changes to the file and compiled the Sass.

To double check all of that, and you can open up the css folder, and you should see your compiled css in a file called main.css. And that is the essence of Grunt. We configure various tasks and then we run them from the terminal. It is a bit weird and hard, but once you get used to how it all fits together, it's an incredibly useful tool.

Gulp is a very similar tool to Grunt, but it uses a different style of configuration and a different approach to running all the tasks behind the scenes. The Gulp config syntax may look bit more familiar to you if you're used to writing JavaScript or jQuery code. And while I've used both Grunt and Gulp, I now favor Gulp for all of my projects.

I just find it a bit more intuitive. For this exercise, I've got another bare bones project set up with an scss folder which has got a main.scss file inside. That's for my Sass, and I've got a css folder for the stars to be compiled into. So the initial Gulp setup follows a very similar process to the Grunt setup.

First, we need to install Gulp globally so that it can be used on any of our projects. And again, this is a one time installation. So if you already have Gulp installed, you can skip this step. To install Gulp globally, we can run the command npm install -g gulp.

We now need to create a package JSON which will list all of the packages that we're gonna need for performing our Gulp tasks. So back in the terminal, run npm init. So having initialized our project, we now need to install a local version of Gulp and the Gulp Sass package.

And we'll save those as dependencies to our packaged JSON. With those packages installed, we're now ready to create our configuration file to set up all of our Gulp tasks. So we'll create a gulpfile.js in the project root, and into that we'll add the following code. Again, just head to atozsass.com and do a bit of copying and pasting if you following along.

Having saved our Gulp file, we now need to run the tasks. So back in the terminal, we can use the Gulp command followed by the task name. To compile our styles, we can run gulp sass, or to watch for changes, we can run the default task just by running Gulp.

We do that in the terminal from the project root or from wherever the Gulp file JS is. If everything is working properly, you should see a main.css file compiled when you add some Sass to your main.scss file and hit save. So what's the difference between Grunt and Gulp and why are the two seemingly identical ways or very similar ways of doing the same thing?

Well, the Gulp syntax is a bit shorter. And I personally find these kind of chained function calls a lot easier to read and a lot easier to follow, rather than having to read through a huge, great big configuration object. Which is what you get with Grunt. But the biggest difference lies in the compiler that is being used behind the scenes with either Grunt Sass or Gulp Sass.

Grunt uses Ruby Sass whereas Gulp uses Node Sass. And Node Sass is a wrapper for LibSass, which all sounds a little bit convoluted. But LibSass is a much faster version of the Sass compiler which has been written in C. On a big project, compiling your Sass with Gulp will be significantly faster than when using Grunt.

And so that alone is the reason that I've switched all of my projects over to Gulp from Grunt. Having gone through the process of setting up either of these tools or both in this case, we can now add additional tasks to help speed up our workflow. Two tools that I could now live without are LiveReload and Autoprefixer.

And while we aren't gonna go through the process of setting them up, I'll just explain what they are now. And if you're interested, I'll leave that as an exercise for you. LiveReload will automatically refresh the browser when any changes are detected to any files that you're watching. Even though the process of refreshing the browser isn't particularly difficult, it is something that I do hundreds of times a day when I'm working on a project.

So it may be a micro-optimization, but it's really, really worth it. Autoprefixer is a post CSS plugin, which runs on your compiled CSS and adds in any vendor prefixes, adds them where they're needed. And it does that as per the data on caniuse.com. This means that I never have to write any prefixes in my Sass.

And it means I can just focus on making stuff rather than faffing around, looking up, or writing out lots of prefixes manually. Whether you prefer Grunt or Gulp, I'd highly recommend looking into this in more detail and automating your workflow wherever possible, as it's just one less thing that you'll have to think about.

