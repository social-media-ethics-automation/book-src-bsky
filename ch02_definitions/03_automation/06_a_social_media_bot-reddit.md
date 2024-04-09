# A program that makes one reddit post
Below is a computer program written in the Python programming language. The program will make a reddit post in the subreddit "soc_media_ethics_auto". The post will be titled "A bot post" and say: "This post was made by a computer program!". Since this is a computer program that posts on reddit, we would call this program a reddit bot.

Don't worry if you don't understand any of this Python code yet; we will build an understanding of code like this throughout the book.

```python
import praw

username="fake_reddit_username"
password="sa@#4*fdf_fake_password_$%DSG#%DG"
client_id="45adf$TW_fake_client_id_JESdsg1O"
client_secret="56sd_fake_client_secret_%Yh%"

reddit = praw.Reddit(
    username=username, password=password,
    client_id=client_id, client_secret=client_secret,
    user_agent="a custom python script"
)

reddit.subreddit(
   "soc_media_ethics_auto"
).submit(
   "A bot post", 
   selftext = "This post was made by a computer program!"
)
```

Though you may not understand anything in the above code yet, I want to point out a couple things:
- The code above is full of English words like "import", "username", "password", and "secret," which may help you guess the meaning of the code.
- There are also other symbols as well, though being used in a different way than in normal English, symbols like ``=``, `_`, `.`, `(`, and `)`
- The final lines of code gives good hints as to what it is doing: `subreddit` chooses which subreddit the post will be made on, and `submit` has the information to submit as a new post.
- There are four pieces of text with random numbers and letters that include things like "username" and "client_secret" inside. These pieces of text are meant to be replaced with your reddit username and password and a pair of special passwords for running a reddit bot. You can get these special passwords if you get developer access to reddit (see the page on [](../../appendix/making_bot_account.md)). Once you put your special passwords in those locations then this code will make a reddit post.

```{figure} bot_post.png
---
name: bot_post_fig
alt: Screenshot of a post on reddit, posted by "kthayer_teacher_bot" titled "a bot post" with the text of "This post was made by a computer program!"
---
A [reddit post](https://www.reddit.com/r/soc_media_ethics_auto/comments/zwm4mw/a_bot_post/) made by running the code above with the account information for "kthayer_teacher_bot".
```

We will go through that example code in more detail next.
