# A program that makes one Discord post

Below is a computer program written in the Python programming language. The program will make a Discord post in the the discord channel that has an id of 123456789 (this is a fake channel number). The post will say: "This post was made by a computer program!". Since this is a computer program that posts on Discord, we would call this program a Discord bot.

Don't worry if you don't understand any of this Python code yet; we will build an understanding of code like this throughout the book.

```python
import discord
import nest_asyncio
nest_asyncio.apply()

discord_token = "m#5@_fake_discord_token_$%Ds"

client = discord.Client(intents=discord.Intents.default())

@client.event
async def on_ready():
    channel_id = 123456789
    channel = client.get_channel(channel_id)
    await channel.send("This post was made by a computer program!")
    await client.close()
    
client.run(discord_token)

```

Though you may not understand anything in the above code yet, I want to point out a couple things:
- The code above is full of English words like "import", "token", "ready", "channel", and "send," which may help you guess the meaning of the code.
- There are also other symbols as well, though being used in a different way than in normal English, symbols like ``=``, `_`, `.`, `:`, `(`, and `)`, as well as some unusual spacing



- The indented lines of code gives good hints as to what it is doing: `get_channel` loads a specific discord channel to post on, and `send` has the information to make as a new post.
- There is one pieces of text with random letters and numbers called the "discord_token" which is basically a password for your discord bot to log in. There is also a piece of text with a number called the "channel_id" which is a number that lets your bot look up a specific discord channel. You can get these special passwords and discord channel ids (see the page on [setting up your discord bot](../../appendix/making_bot_account.md)).. Once you put your special token and channel ids in those locations, then this code will make a discord post

```{figure} discord_bot_post.png
---
name: bot_post_fig
alt: Screenshot of a post on discord, posted by "info_103_teaching_example_app" with the text of "This post was made by a computer program!"
---
A discord post made by running the code above with the account information for "info_103_teaching_example_app".
```

We will go through that example code in more detail next.
