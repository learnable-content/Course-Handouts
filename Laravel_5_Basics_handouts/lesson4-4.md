![](headings/4.4.png)

Another important feature is **factory**. Factory is new to Laravel 5 and before it came about, we did pretty much everything in seeds. Factories already have the Faker inside of it. So one of the things we could do is we could setup this post table.

This post table seeder inside of factories, and then consume it. So it's like here's the setup for a user. Whenever I want to do a user or create a user, like a fake user, I can use this factory. And then it does the faker name, the faker safe email, and password, and things like that for us.

And then here in the seeder I can consume that. The reason why this was kind of broken out too, and one of the other things. That kind of makes this easier is that once we have the setup for a user we can consume it as a seeder. Or here in the seeder file.

But the other thing that we can do is we can actually test it. So we're not talking about test in this series, but here in the test folder, you could actually with a test, go create a user. It's gonna look for this model factory, tell it to use this model factory as kind of like the setup for user.

And then have that user create a post and then test to see if that worked out. But here we're gonna create a new seeder, and we're gonna create a user seeder so that we can kind of see how to use factories just a bit. I still have my tinker open here, I'm gonna exit that.

And then I'm gonna do php artisan make:seeder. And then I'm gonna say UsersTableSeeder. That got created and here it is right here. Gonna go in and look at the documentation. So that way we can see here, here it looks a little convoluted here. You can see that there's other stuff that we're doing here to kinda like create 50 users.

And then each one of those users is gonna make a post and stuff like that. But really all we're concerned with is this right here. This factory, factory app user, there, create up to there. Should be able to just do that. So here I'm saying I want to be able to use this factory in, let me see if I have to call this.

So here in UsersTableSeeder, I'm saying factory, I want app, User::class. I want 50 of them that I want created. So 50 users, and you can tell looking at my code it's like I used this. I had to tie these in, I did a loop so that we could create each one.

Here it's factory(App/User::Class, 50)->create(); And then the other thing you need to do, is remember inside of here, we'll call seeders. So, UsersTableSeeder, php artisan migrate:refresh meaning get rid of all the data and I want you to seed it as well. Post table to seeder, that was great. Let's see what happens here with the UsersTableSeeder.

Okay, that passed as well. Here I'm going to refresh. I still have my 500 posts here. Go to users and I have 50 users with 50 passwords. Here I have Brant Dosh and then his email, and then the rest of these fake people's email. But as you can see I used the factories to do so instead of doing it the other way that I showed you here with the post tables.

Here, this was a little bit more manual, I had to include the library. Here in model factory, it's like we created the factory, here it's like, here's the structure of the data. And then here, I just called factory(App/User::Class), 50 I want you to create. So factories is a cool thing.

Be sure to read up on it here on how to create your factory for post. And then the other thing behind it is that we can actually. If you click on this link here, it shows you here a little bit more about testing, and how we can test, and how factories kind of help with that.

