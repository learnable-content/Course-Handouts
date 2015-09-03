![](headings/2.2.png)

# Adding UI Elements

We're going to add UI elements to our different scenes (currently we only have two). First of all, resize scenes to an iPhone because that's what we're going to be developing against in this course. 

Click on the first scene and then on the attributes inspector. If you don't have that panel, open it by going to View > Assistant Editor > Show Assistant Editor. Next select Size, Inferred is going to be a 4.7, for an iPhone 6. Do the same for the second scene.

You will also notice the Tab Bar Controller, but don't worry about that. It's actually not going to be visible to the user - it is there to provide the tabbing functionality.

Now let's give our scenes some real names. The first one will be called "Activity" and the second one - "Performance". To rename the scene:

* Click on the tab.
* Attributes list will be presented.
* Change Title to the desired value.

# Creating Scenes

Open up your document outline where you can get bit more information about the scenes. Grab the second tab, drag it out onto the storyboard and drop it. Put this new scene on top of the other one. Also name this scene "Add Activity". You'll notice we're missing our tab bar - we'll take care of that in a little bit.

# Adding Labels

Now let's start adding UI elements onto these scenes.

What I want now is a UI Picker View. Drag that up onto your scene and size it so it's got a width equal to the view's width. Now let's add a countdown label. The text of this label should be "0". Change the size of it to something fairly big.

Now on the Performance scene, we're going to have a table. We'll be able to scroll through our different activities that we have and it's also going to display the time that we've been involved with those activities.

So delete the filler labels that come with the scenes. Then in the object library type in "table" to find a Table View. Drag that on the view and fill the width. Adjust the height so that there is a room at the top for the status bar. Also leave some room at the bottom so that the tab bar is not hidden.

Now build the Add Activity. Remove all its items and add a label. Call it Activity Name. Then drag on a text field. This field will be used to type in the the name of an activity and. We'll also need a button so that a user save that activity. So type in "button" in the UI Picker View and drag a button onto the scene. Call it "Save Activity".

# Testing

If you need to run your project, just select "iPhone 6" from the menu and click "Run". You'll notice that our third view is not linked anywhere, but we'll fix that in the next step.