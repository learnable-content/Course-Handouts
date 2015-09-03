![](headings/2.3.png)

# Adding the Third Scene

In this step we're going to add our third scene to the tab functionality.

The first thing I want to do is add a navigation item. Search for a "tab bar" item and drag it onto the view. Now we need to link this to our tab board controller. Click on the `Ctrl` key and then drag up to our Add Scene. Select "view controllers" under Relationship Segue. What we've done is established a relationship between the tab bar view controller and our add scene as well.

# Testing the App

Boot up the application to see these it in action. You should be able to transit between different views.

# Storyboard

The "Storyboard entry point" is for our TabViewController. We don't see the tab bar controller, but you can see behind the scenes how it's actually gluing all of this together, and allowing us to do this tabbing functionality. So again, in tiling, what we did, we did not have a relationship established between our tab work controller, and our add scene. I held down the `Ctrl` key which allowed me to create the connection and connected it to our add scene.

In our storyboard, we can see three scenes, and we have our different segue connections. The storyboard is where you develop your user interface, where you put all your scenes together, and you can see all your different scenes on here, and as you get more you'll be able to scroll through and you'll be able to see those kinds of scenes. We haven't actually started typing in any code, we've not actually done anything with Swift. Still, we've created our UI and when we run the application, we can see basically our finished product really quick. That's a good thing to do if you have a simple app or if you have a simple UI, to just go ahead and put your UI together in your storyboards. Without any code, you can create these kinds of transitions so that you then can go from one scene to another and see some functionality in your app without having to go behind the scenes into Swift and code anything up.