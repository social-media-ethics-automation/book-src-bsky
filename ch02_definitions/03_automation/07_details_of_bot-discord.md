# Understanding the Discord Bot Code

Let's look more at that program that creates one Discord post.

There are a number of ways of looking at the code, but first, let's look at it as a template with a couple pieces we can change.

## The program as a template

Below I've highlighted the text of the sections of the program that you might want to modify.

<pre style="color:gray">
import discord
import nest_asyncio
nest_asyncio.apply()

discord_token = "<strong style="color:black;background-color:lightgreen">m#5@_fake_discord_token_$%Ds</strong>"

client = discord.Client(intents=discord.Intents.default())

@client.event
async def on_ready():
    channel_id = <strong style="color:black;background-color:lightgreen">123456789</strong>
    channel = client.get_channel(channel_id)
    await channel.send("<strong style="color:black;background-color:lightgreen">This post was made by a computer program!</strong>")
    await client.close()
    
client.run(discord_token)
</pre>

The first highlighted pieces of code is the discord token (your bot's special passwords), so your bot can log in. You can get when you get those passwords by following these steps to get [developer access to reddit](../../appendix/making_bot_account.md) (I've put fake values in them for now).

The second highlighted piece of code is the id number for the discord channel you want to post to. Instructions for getting a channel's id number are also on the [developer access to reddit page](../../appendix/making_bot_account.md)

The final highlighted pieces of code is what text to post to Discord.

So, by changing those sections of code, you run this program to post whatever message you want to post on the Discord channel of your choosing. It is, of course, much easier to just open Discord and post something, but as we get to more complicated programs, we'll start to see more of the power (and pitfalls) of automation on social media.

_Note: two of the highlighted sections of code are surrounded by double quotes. In the Python programming language, putting something in quotes indicates that you want the computer to think of the things inside the quotes as pieces of text, in this case passwords and reddit post information. The highlighted code that doesn't have quotes is a number._

## Adding code comments

The goal of programming language code is to be readable by both humans and computers, but sometimes the meaning of code isn't always clear to humans trying to read it. In order to aid humans reading the code, programming languages allow programmers to do things to make the code more readable, such as adding extra blank lines between sections of code. Blank lines can be used to have some lines of code be visually grouped together, and some be separated, so humans can better follow the outline of the code. (We'll add or remove some blank lines to emphasize different things in the code below).

Most programming languages also allow "comments," which are pieces of code that the computer will ignore. These comments allow the person writing the code to leave a note to future people reading the code, knowing that the computer won't read it (like an [aside](https://en.wikipedia.org/wiki/Aside) {cite:p}`Aside2023` in a play).

In Python, you can add a comment by using the `#` symbol. Python will ignore everything on a line that comes after the `#`. But human programmers will often look for the meaning of the program in these comments.

So, in order to make the program above easier for future humans to understand, let's add three comments telling these future humans where to add their special bot password, where to put the id for the Discord channel to post to, and where they can change the text of the post:

```python
import discord
import nest_asyncio
nest_asyncio.apply()

# TODO: put the discord token for your bot below
discord_token = "m#5@_fake_discord_token_$%Ds"

client = discord.Client(intents=discord.Intents.default())

@client.event
async def on_ready():
    # TODO: put the discord channel id number below
    channel_id = 123456789

    channel = client.get_channel(channel_id)

    # TODO: put the message you want to post to discord below
    await channel.send("This post was made by a computer program!")

    await client.close()
    
client.run(discord_token)
```

With those, hopefully a future human reader will have a better chance of understanding how to modify the program to do what they want.

_Note: I started each comment with "TODO" to tell the future human that there is a task they have **to do** to get the program to work for them. Since this is only intended for human readers, I could have written it in any way I want, but all capital letter TODOs are commonly used like this by programmers._


## Purpose of each section of code

Now that we've looked at the code as a modifiable template, let's break the code into sections and look at what the purpose of each part is. The code is run starting at the top and going down from there, so we will go through the code in that order.

_Note: It's normal if you don't understand everything here. Over the course of this book you will learn to understand more of how programs work, but also, even professional programmers often don't understand parts of the programs they are working on, they just understand enough to modify the parts they need to._

The first lines of code is:
```python
import discord
import nest_asyncio
nest_asyncio.apply()
```

The purpose of these line of code that loads other sets of code. The first code it loads is called [discord.py](https://discordpy.readthedocs.io/en/stable/) {cite:p}`WelcomeDiscordPy`, which is code specially written to help make programs that work with Discord. It next loads a library `nest_asyncio` that helps our bots run correctly in Jupyter Notebooks, and the next line applies that library to the rest of the code we run.


The next section of code is two lines long:
```python
discord_token = "m#5@_fake_discord_token_$%Ds"
client = discord.Client(intents=discord.Intents.default())
```

This is code is starting the setup of our bot. It first line of code stores the discord token, so our bot can log in (Again, you'll have to get your actual discord token for your bot and replace the fake one currently in the code). Then second line of code it creates a bot program with some default settings.

The next section of code is six lines long (plus two added blank lines to help group related actions):

```python
@client.event
async def on_ready():
    channel_id = 123456789
    channel = client.get_channel(channel_id)

    await channel.send("This post was made by a computer program!")

    await client.close()
```

The purpose of this code is to provide instructions for what your discord bot should do once it has logged in, specifically to make a post to a given channel and then close the bot.

The first two lines (`@client.event` and `async def on_ready():`) are just an indication that these are instructions for what the bot should do once it has logged in. Note: `def` means define, and `on_ready` means we are defining what the bot should do once it is ready (that is, logged in). The rest of the lines in this section are indented, indicating that they are the things we want the bot to do once it is logged in and ready.

The next two lines of code (`channel_id = 123456789` and `channel = client.get_channel(channel_id)`) are for loading a specific discord channel. The first line is where a specific channel id is saved into python, and the second line is where the `discord` code finds that specific channel.

The next line of code is what actually makes the post on the given channel (`await channel.send("This post was made by a computer program!")`). 

The final line of code in this section (`await client.close()`) tells the bot to shut down (note: there are other ways of writing bots where they keep running so that they can do things like automatically reply to someone).

The final section of the code is this one line:
```python
client.run(discord_token)
```

This code uses the discord_token that was saved into Python to start running the bot, which will log in and then do the actions that we defined above to do once the bot is ready (find a channel, post to it, and close the bot).

## Adding more code comments
Now that we've looked at the purpose of each section of code, we can copy our bot code one more time, now adding comments explaining what each section does, so that future humans reading the code are more likely to understand it.

Following the common practice of programmers, we will put the comment before the section of code that the comment is explaining. We can also make multiple comment lines as needed if our comments are long.

```python
# Load some code called "discord" that will help us work with Discord
import discord

# Load another library that helps the bot work in Jupyter Noteboook
import nest_asyncio
nest_asyncio.apply()

# Set up your Discord connection
# TODO: put the discord token for your bot below
discord_token = "m#5@_fake_discord_token_$%Ds"
client = discord.Client(intents=discord.Intents.default())

# Provide instructions for what your discord bot should do once it has logged in
@client.event
async def on_ready():
    # Load the discord channel you want to post to
    # TODO: put the discord channel id number below
    channel_id = 123456789
    channel = client.get_channel(channel_id)

    # Post a message to your discord channel
    # TODO: put the message you want to post to discord below
    await channel.send("This post was made by a computer program!")

    # Tell your bot to stop running
    await client.close()


# Now that we've defined how the bot should work, start running your bot
client.run(discord_token)
```

Now that we've looked over the code and commented it, let's go to the next page, where you can try running it!
