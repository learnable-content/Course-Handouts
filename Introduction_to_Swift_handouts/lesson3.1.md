![](headings/3.1.png)

# What Is MVC

iOS apps are built off of a framework, or an architectural framework called **MVC (Model View Controller)**.

# View

The **view** is basically what you see inside the app; in Xcode this is going to be storyboards. You can create view elements in the code behind, and have them come through, in sight of the view so that you can begin seeing them. That's more of an advanced kind of thing. You might create UI elements dynamically and then put them into the view based on certain events that the user has done.

But for us, we're just going to stick to a little bit of more simpler architectures, so we can just use storyboards. On storyboards, you're grabbing UI objects from the object library (like labels, text boxes, buttons etc).

# Controller

The **controller** is sits in the middle between the view and the model. Basically it's the conduit between any model classes and the view. The view doesn't talk directly to the model in most cases, because we're separating kind of the responsibilities in our architecture. So for the view it's a little disconnected from what the model is doing. We allow the controller to handle the communication between those two.

# Model

**Models** are the custom classes you might create. It could be a recipe class where it's able to hold instances of a recipe. This recipe class is really a structure that you can add, say a recipe name, the actual recipe content, a photo. So the recipe model is like a manager that allows you to add a recipe to your array of recipes, remove it from the array, load it from a web service or a database.