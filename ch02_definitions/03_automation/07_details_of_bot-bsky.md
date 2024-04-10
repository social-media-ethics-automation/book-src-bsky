# Understanding the Bluesky Bot Code

Let's look more at that program that creates one Bluesky post.

There are a number of ways of looking at the code, but first, let's look at it as a template with a couple pieces we can change.

## The program as a template

Below I've highlighted the text of the sections of the program that you might want to modify.

<pre style="color:gray">
from atproto import Client

client = Client(base_url="https://bsky.social")
client.login("<strong style="color:black;background-color:lightgreen">your_account_name.bsky.social</strong>", "<strong style="color:black;background-color:lightgreen">m#5@_fake_bsky_password_$%Ds</strong>")

client.send_post("<strong style="color:black;background-color:lightgreen">This post was made by a computer program!</strong>")
</pre>

The first two highlighted pieces of code are for your Bluesky handle (e.g. something.bsky.social) and password (note: If you make your account at a different domain name than the default "bsky.social," then you'd also need to change the part above that has `https://bsky.social`). You can create a Bluesky account by [following the steps here](../../appendix/making_bot_account.md) (I've put fake values in them for now):
- handle
- password

The final highlighted piece of code is the text to post to Bluesky. You can change the text of these values to change what text to post.

So, by changing those sections of code, you run this program to post whatever you want to post on Bluesky. It is, of course, much easier to just open Bluesky and post something, but as we get to more complicated programs, we'll start to see more of the power (and pitfalls) of automation on social media.

_Note: all the highlighted sections of code are surrounded by double quotes. In the Python programming language, putting something in quotes indicates that you want the computer to think of the things inside the quotes as pieces of text, in this case passwords and reddit post information._

## Adding code comments

The goal of programming language code is to be readable by both humans and computers, but sometimes the meaning of code isn't always clear to humans trying to read it. In order to aid humans reading the code, programming languages allow programmers to do things to make the code more readable, such as adding extra blank lines between sections of code. Blank lines can be used to have some lines of code be visually grouped together, and some be separated, so humans can better follow the outline of the code.

Most programming languages also allow "comments," which are pieces of code that the computer will ignore. These comments allow the person writing the code to leave a note to future people reading the code, knowing that the computer won't read it (like an [aside](https://en.wikipedia.org/wiki/Aside) {cite:p}`Aside2023` in a play).

In Python, you can add a comment by using the `#` symbol. Python will ignore everything on a line that comes after the `#`. But human programmers will often look for the meaning of the program in these comments.

So, in order to make the program above easier for future humans to understand, let's add two comments telling these future humans where to add their special passwords and where they can change the text of the post:

```python
from atproto import Client

# TODO: put your account name and password below
client = Client(base_url="https://bsky.social")
client.login("your_account_name.bsky.social", "m#5@_fake_bsky_password_$%Ds")

# TODO: modify the text in the quotes below to change what this bot posts to Bluesky:
client.send_post("This post was made by a computer program!")
```

With those, hopefully a future human reader will have a better chance of understanding how to modify the program to do what they want.

_Note: I started each comment with "TODO" to tell the future human that there is a task they have **to do** to get the program to work for them. Since this is only intended for human readers, I could have written it in any way I want, but all capital letter TODOs are commonly used like this by programmers._


## Purpose of each section of code

Now that we've looked at the code as a modifiable template, let's break the code into sections and look at what the purpose of each part is. The code is run starting at the top and going down from there, so we will go through the code in that order.

_Note: It's normal if you don't understand everything here. Over the course of this book you will learn to understand more of how programs work, but also, even professional programmers often don't understand parts of the programs they are working on, they just understand enough to modify the parts they need to._

The first line of code is:
```python
from atproto import Client
```

The purpose of this line of code that loads another set of code. The it loads is called [atproto](https://atproto.blue/), which is short for "The AT Protocol SDK for Python," and is code specially written to help make programs that work with Bluesky's [AT Protocol](https://atproto.com/). From this code, we specifically load the [Client](https://atproto.blue/en/latest/atproto_client/index.html) section of code, which is what lets us login to an account and perform actions.


The next section of code is two lines long:
```python
client = Client(base_url="https://bsky.social")
client.login("your_account_name.bsky.social", "m#5@_fake_bsky_password_$%Ds")
```

The purpose of this code is to connect to Bluesky and login with your username and password. Again, you'll have to replace our fake usernames and passwords with your actual username and password in the code if you want it to work with your account.

The final lines of code is:
```python
client.send_post("This post was made by a computer program!")
```

This is the line of code where a Bluesky post is actually made. The new post will have the text that is inside the quotation marks.

## Adding more code comments
Now that we've looked at the purpose of each section of code, we can copy our bot code one more time, now adding comments explaining what each section does, so that future humans reading the code are more likely to understand it.

Following the common practice of programmers, we will put the comment before the section of code that the comment is explaining. We can also make multiple comment lines as needed if our comments are long.

```python
# Load some code called "Client" from the "atproto" library that will help us work with Bluesky
from atproto import Client

# Login to Bluesk
# TODO: put your account name and password below
client = Client(base_url="https://bsky.social")
client.login("your_account_name.bsky.social", "m#5@_fake_bsky_password_$%Ds")

# Send a Bluesky post
# TODO: modify the text in the quotes below to change what this bot posts to Bluesky:
client.send_post("This post was made by a computer program!")
```

Now that we've looked over the code and commented it, let's go to the next page, where you can try running it!
