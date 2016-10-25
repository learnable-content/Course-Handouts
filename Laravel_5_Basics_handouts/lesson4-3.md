![](headings/4.3 .png)

PHP Artisan is a very useful tool to interact with your app. Use `php artisan tinker` to open it. To find a post with an id of `1` you can say

```
$post = Post::find(1);
```

You'll get "Class Post not found" error. Remember that everything is namespaced, so say

```
$post = App\Post::find(1);
```

To echo the title, say

```
$post->title;
```

So basically we are pulling data from the database with PHP Artisan Tinker.

Create a post:

```
Post::create(
    [
        'title' => "This is awesome",
        'body' => "lorem ipsum awesome"
    ]
);
```

You'll get a "MassAssignment error". So that might be something that we need to do inside of our model here. I'm glad we're running into these because these are things that are kind of, they're little gotchas and you tend to forget about them inside of Laravel. But it's this thing called fillable here.

So inside my application, yeah, I can interact with my app with Faker. But outside of it, it's like, hey, you don't have access to this, there's no way. And it's a layer of protection for us. So here I'm gonna copy this thing from, well, here, we'll just kinda do it, it's just an array.

I'm just going to use this for looking, okay, yada yada yada, MassAssignment. Okay, we'll copy it. I made up my mind. These attributes are for MassAssignment fillable. I want you to be able to fill in title, and I want you to be able to fill in password, I mean, sorry, body.

So these are the things that I want to be able to fill in, mass assign, meaning that from any point in my application, to post. And this is just a layer of protection for us. So here let's just pretend like there's some column I don't want to be able to give access to, and that's what I would do.

Notice here in User, any time that I return a user data, I don't want to return password, and I want to hide, and with this hidden, I want to hide password and want to hide the remember token. So here we go back to the app, I hit the up arrow, hit Return.

And it could very well be that I might need to do this over again, because I just changed that. So App\Post. Yeah, there it is. There we go. So I needed to restart Tinker for that to work. Here, I'm gonna go here and I'm gonna refresh this data, and I'm gonna look, and we should have 501, 501, the bottom record, this is awesome.

So just to let you know, we are able to interact with our application. PHP Artisan Tinker inside it. I mean, Tinker alone is a tool on its own, but when it's inside of Laravel, we're able to interact with our application by retrieving data, doing stuff with it if we wanted to do stuff with it.

Maybe there's some cool thing that we want to try out by pulling the data out, or maybe we wanna tie it to something else. Like I said before, this is where I kind of test those things out. And once I got the kind of line of code that works the way I want it to work, I'll take it over either to the controller, or wherever I want inside the application.

