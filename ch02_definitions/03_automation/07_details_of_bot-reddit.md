# Understanding the Reddit Bot Code

Let's look more at that program that creates one Reddit post.

There are a number of ways of looking at the code, but first, let's look at it as a template with a couple pieces we can change.

## The program as a template

Below I've highlighted the text of the sections of the program that you might want to modify.

<pre style="color:gray">
import praw

username="<strong style="color:black;background-color:lightgreen">fake_reddit_username</strong>"
password="<strong style="color:black;background-color:lightgreen">sa@#4*fdf_fake_password_$%DSG#%DG</strong>"
client_id="<strong style="color:black;background-color:lightgreen">45adf$TW_fake_client_id_JESdsg1O</strong>"
client_secret="<strong style="color:black;background-color:lightgreen">56sd_fake_client_secret_%Yh%</strong>"

reddit = praw.Reddit(
    username=username, password=password,
    client_id=client_id, client_secret=client_secret,
    user_agent="a custom python script"
)

reddit.subreddit(
   "<strong style="color:black;background-color:lightgreen">soc_media_ethics_auto</strong>"
).submit(
   "<strong style="color:black;background-color:lightgreen">A bot post</strong>", 
   selftext = "<strong style="color:black;background-color:lightgreen">This post was made by a computer program!</strong>"
)


</pre>

The first four highlighted pieces of code are for the special passwords that let you run a bot. You can get when you get those passwords by following these steps to get [developer access to reddit](../../appendix/making_bot_account.md) (I've put fake values in them for now):
- username
- password
- client_id
- client_secret

The final three highlighted pieces of code are the information for what to post on reddit. First, in the parentheses after `subreddit` is which subreddit to post on. In the parentheses after the `submit` is first the title of the post, and next is the text of the post itself. You can change any of these values ot change which subreddit you post to, and what title and text to post.

So, by changing those sections of code, you run this program to post whatever reddit you want to post on a subreddit. It is, of course, much easier to just open reddit and post something, but as we get to more complicated programs, we'll start to see more of the power (and pitfalls) of automation on social media.

_Note: all the highlighted sections of code are surrounded by double quotes. In the Python programming language, putting something in quotes indicates that you want the computer to think of the things inside the quotes as pieces of text, in this case passwords and reddit post information._

## Adding code comments

The goal of programming language code is to be readable by both humans and computers, but sometimes the meaning of code isn't always clear to humans trying to read it. In order to aid humans reading the code, programming languages allow programmers to do things to make the code more readable, such as adding extra blank lines between sections of code. Blank lines can be used to have some lines of code be visually grouped together, and some be separated, so humans can better follow the outline of the code.

Most programming languages also allow "comments," which are pieces of code that the computer will ignore. These comments allow the person writing the code to leave a note to future people reading the code, knowing that the computer won't read it (like an [aside](https://en.wikipedia.org/wiki/Aside) {cite:p}`Aside2023` in a play).

In Python, you can add a comment by using the `#` symbol. Python will ignore everything on a line that comes after the `#`. But human programmers will often look for the meaning of the program in these comments.

So, in order to make the program above easier for future humans to understand, let's add two comments telling these future humans where to add their special passwords and where they can change the text of the post:

```python
import praw

# TODO: Put your reddit username, password, and special developer access passwords below:
username="fake_reddit_username"
password="sa@#4*fdf_fake_password_$%DSG#%DG"
client_id="45adf$TW_fake_client_id_JESdsg1O"
client_secret="56sd_fake_client_secret_%Yh%"

reddit = praw.Reddit(
    username=username, password=password,
    client_id=client_id, client_secret=client_secret,
    user_agent="a custom python script"
)



# TODO: modify the text in the quotes below to change what and where this bot posts to reddit:
reddit.subreddit(
   "soc_media_ethics_auto"
).submit(
   "A bot post", 
   selftext = "This post was made by a computer program!"
)

```

With those, hopefully a future human reader will have a better chance of understanding how to modify the program to do what they want.

_Note: I started each comment with "TODO" to tell the future human that there is a task they have **to do** to get the program to work for them. Since this is only intended for human readers, I could have written it in any way I want, but all capital letter TODOs are commonly used like this by programmers._


## Purpose of each section of code

Now that we've looked at the code as a modifiable template, let's break the code into sections and look at what the purpose of each part is. The code is run starting at the top and going down from there, so we will go through the code in that order.

_Note: It's normal if you don't understand everything here. Over the course of this book you will learn to understand more of how programs work, but also, even professional programmers often don't understand parts of the programs they are working on, they just understand enough to modify the parts they need to._

The first line of code is:
```python
import praw
```

The purpose of this line of code that loads another set of code. The code it loads is called [praw](https://praw.readthedocs.io/en/stable/) {cite:p}`PRAWDocumentation` (The Python Reddit API Wrapper), which is code specially written to help make programs that work with Reddit.


The next section of code is four lines long:
```python
username="fake_reddit_username"
password="sa@#4*fdf_fake_password_$%DSG#%DG"
client_id="45adf$TW_fake_client_id_JESdsg1O"
client_secret="56sd_fake_client_secret_%Yh%"
```

This is code to store all of the reddit password information we need to use a bot. You need your reddit username and password, and then a special client_id and client_secret for the bot. Again, you'll have to get your actual developer access passwords and replace the fake ones currently in the code.

The next section of code is five lines long:

```python
reddit = praw.Reddit(
    username=username, password=password,
    client_id=client_id, client_secret=client_secret,
    user_agent="a custom python script"
)
```

The purpose of this code is to take all the developer access passwords you entered above, and give them to the praw code so that the praw code can log into your reddit account and provide the needed passwords for running a reddit bot. 

Note that the last line is setting the `user_agent` which is a description of which program is being used to post from. For example, it might be "Reddit web page" or "Reddit iPhone app" or "Sprout social media manager." For our programs, I've just labeled our posts as being from "a custom python script."

The final lines of code are:
```python
reddit.subreddit(
   "soc_media_ethics_auto"
).submit(
   "A bot post", 
   selftext = "This post was made by a computer program!"
)
```

These are the lines of code where a reddit post is actually made. First, the `subreddit` section selects which subreddit an action will be taken on, and then `submit` creates a new post with the given title and text.

## Adding more code comments
Now that we've looked at the purpose of each section of code, we can copy our bot code one more time, now adding comments explaining what each section does, so that future humans reading the code are more likely to understand it.

Following the common practice of programmers, we will put the comment before the section of code that the comment is explaining. We can also make multiple comment lines as needed if our comments are long.

```python
# Load some code called "praw" that will help us work with reddit
import praw

# Load all your developer access passwords into Python
# TODO: Put your reddit username, password, and special developer access passwords below:
username="fake_reddit_username"
password="sa@#4*fdf_fake_password_$%DSG#%DG"
client_id="45adf$TW_fake_client_id_JESdsg1O"
client_secret="56sd_fake_client_secret_%Yh%"

# Give the praw code your reddit account info so
# it can perform reddit actions
reddit = praw.Reddit(
    username=username, password=password,
    client_id=client_id, client_secret=client_secret,
    user_agent="a custom python script"
)

# Post a reddit post
# TODO: modify the text in the quotes below to change what and where this bot posts to reddit:
reddit.subreddit(
   "soc_media_ethics_auto"
).submit(
   "A bot post", 
   selftext = "This post was made by a computer program!"
)
```

Now that we've looked over the code and commented it, let's go to the next page, where you can try running it!
