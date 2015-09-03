![](headings/4.3.png)

# Intro

We're going to create a scene where we can add an activity to our application.ch shows us all the different activities and their total times,and here's our add scene.

# Adding a Scene and View Controllers

Now we need an `AddViewController` to do manipulations to our add scene. This view controller is going to particularly allow us to capture the user's input when they type in an activity name and then click the add button. Therefore create a new view controller and call it `AddViewController`. Now bind your scene to the view controller. Next create a text field IB Outlet, call it `ActivityLabel`; connect that.

# Removing the Keyboard

We need another protocol - `UITextFieldDelegate`. Go ahead and test out this functionality.

# Adding an Activity

We're going to need a `viewDidAppear` inside of the performance view controller. Remember that it happens each time the view is displayed.

```swift
override func viewDidAppear(animated: Bool) {
    super.viewDidAppear(animated)
   tableView.reloadData()
}
```

We're going to need an IB outlet here as well for our table view, so create it. Now give it a try.

# Testing the App

```swift
func tableView(tableView: UITableView, canEditRowAtIndexPath indexPath: NSIndexPath) -> Bool {
    if(ActivityManager.activities.count > 1){
        return true
    }
    return false
}
```

`canEditRowAtIndexPath` wants to know, do we have more than one item? If we do, we're going to enable editing, otherwise disable editing by returning `false`.

The next function that we need is the `tableView`:

```swift
func tableView(tableView: UITableView, commitEditingStyle editingStyle: UITableViewCellEditingStyle, 	forRowAtIndexPath indexPath: NSIndexPath) {
    if(editingStyle == .Delete){
        ActivityManager.activities.removeAtIndex(indexPath.row)
        tableView.deleteRowsAtIndexPaths([indexPath], withRowAnimation: .Fade)
    }
}
```

Basically when the user swipes a row, the delete button will appear and the user can then click to delete it.