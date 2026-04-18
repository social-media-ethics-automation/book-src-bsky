# A program that makes one Mastodon post

Below is a computer program written in the Python programming language. The program will make a Mastodon post. The post will say: "This post was made by a computer program!". Since this is a computer program that posts on Mastodon, we would call this program a Mastodon bot.

Don't worry if you don't understand any of this Python code yet; we will build an understanding of code like this throughout the book.

```python
from mastodon import Mastodon

mastodon = Mastodon(
    api_base_url = "https://mastodon.social", 
    access_token = "m#5@_fake_access_token_$%Ds")

mastodon.toot("This post was made by a computer program!")
```

Though you may not understand anything in the above code yet, I want to point out a couple things:
- The code above is full of English words like "import", "access", "token", and "toot," which may help you guess the meaning of the code.
- There are also other symbols as well, though being used in a different way than in normal English, symbols like ``=``, `_`, `.`, `:`, `(`, and `)`, as well as some unusual spacing



- The indented lines of code gives good hints as to what it is doing: `Mastodon(...)` where the instance name (mastodon.social) and the access_token are given is where your Mastodon bot logs in, and `toot` has the information to make as a new post.
- Note that the line with `Mastodon` is where you would put your Mastodon "access token" (see the page on [setting up your Bluesky bot](../../appendix/making_bot_account.md)). Once you put your own "access token"  in that locations, then this code will make a Mastodon post

```{figure} mastodon_bot_post.png
---
name: mastodon_bot_post_fig
alt: Screenshot of a post on Mastodon, posted by "@info103_teacher@mastodon.social" with the text of "This post was made by a computer program!"
---
A Mastodon post made by running the code above with the account information for "@info103_teacher@mastodon.social".
```

We will go through that example code in more detail next.
