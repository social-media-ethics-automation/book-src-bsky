# A program that makes one Bluesky post

Below is a computer program written in the Python programming language. The program will make a Bleusky post. The post will say: "This post was made by a computer program!". Since this is a computer program that posts on Bluesky, we would call this program a Bluesky bot.

Don't worry if you don't understand any of this Python code yet; we will build an understanding of code like this throughout the book.

```python
from atproto import Client

client = Client(base_url="https://bsky.social")
client.login("your_account_name.bsky.social", "m#5@_fake_bsky_password_$%Ds")

client.send_post("This post was made by a computer program!")
```

Though you may not understand anything in the above code yet, I want to point out a couple things:
- The code above is full of English words like "import", "login", "post", and "send," which may help you guess the meaning of the code.
- There are also other symbols as well, though being used in a different way than in normal English, symbols like ``=``, `_`, `.`, `:`, `(`, and `)`, as well as some unusual spacing



- The indented lines of code gives good hints as to what it is doing: `login` is where you login to your Bluesky account, and `send_post` has the information to make as a new post.
- Note that the line with `login` is where you would put your Bluesky account handle (login name) and your password (see the page on [setting up your Bluesky bot](../../appendix/making_bot_account.md)). Once you put your own handle and password in those locations, then this code will make a discord post

```{figure} bsky_bot_post.png
---
name: bsky_bot_post_fig
alt: Screenshot of a post on Bluesky, posted by "info103-teacher.bsky.social" with the text of "This post was made by a computer program!"
---
A Bluesky post made by running the code above with the account information for "info103-teacher.bsky.social".
```

We will go through that example code in more detail next.
