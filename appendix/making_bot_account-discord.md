# Making a Bot Account (Discord)

In using this textbook, you will have opportunities to create and run social media bots. Here we will run through how to create a Discord account and set it up for running your own bots.

While we have made a fake version of Discord for you to test all the code in this book, we highly encourage you to make a Discord bot account and try it out for real!

## Sign up for Discord
[https://discord.com/register](https://discord.com/register)

We suggest making a new, separate Discord account, just for making Discord bots, since you don't want to accidentally get your main Discord account banned or labeled as a bot. Also we suggest using a different password than you use for other accounts, since you might accidentally share it with your code.

Note: If you want to make a new account and you already have one, you may need to sign out from your current account, use a different email address, or use a different web browser (e.g., Mozilla, Google Chrome, Microsoft Edge, Safari).

## Create your own Discord Server
It is easiest to test your bot by creating your own discord server.

```{figure} discord_create_server.png
---
name: discord_create_server_fig
width: 400px
alt: "Screenshot of the discord interface with the \"+\" add a server button highlighted, and then in the menu under \"Create a server\", the \"Create my own\" button is highlighted."
---
Create a Discord server
```


## Create a Discord "Application"

_Note: Instructions are based on the official instructions here: https://discord.com/developers/docs/getting-started_

In order for your bot to run, you must create a Discord "Application." Go to the [Discord Developer Portal](https://discord.com/developers/) and click "New Application":

```{figure} discord_new_app_button.png
---
name: discord_new_app_button_fig
alt: "Screenshot of the discord developer panel, with the \"application\" tab open, and the \"New Application\" button circled."
---
Create a new application in the developer portal.
```

Make up a name for your app and press the "Create" button:

```{figure} discord_create_app.png
---
name: discord_create_app_fig
width: 300px
alt: "Screenshot of the discord create app dialog, with the name for the app being \"soc_media_bot_teaching_demo\""
---
Make up a name for your application (the name of your bot).
```

## Get Discord Token
In order to make your bot work, you'll need to create a special password for your bot to use, which is called a "token." Reset your token and save it somewhere (e.g., email it to yourself). You'll need it later to let your bot log in.

```{figure} discord_generate_token.png
---
name: discord_generate_token_fig
width: 400px
alt: "Screenshot of discord developer application screen with Bot tab selected and the \"Reset Token\" button circled."
---
Reset your token and save it somewhere.
```

## Get Bot Invite Link
Next we need to create an invite link so your bot can be added to different discord servers. 

To do this use the OAuth2 tab for your application. First, set Authorization method to "In-app Authorization." 

```{figure} discord_set_oath_inapp_authorize.png
---
name: discord_set_oath_inapp_authorize_fig
alt: "Screenshot of discord developer application screen with OAuth2 General tab selected and the \"Authorization Method\" dropdown opened with the \"In-app Authorization\" option circled."
---
Set Authorization method to "In-app Authorization."
```


Doing this will give you a bunch of options for permissions your bot might need. We've selected a good starting set of permissions to let you do most things you'll probably want to do with your bot.

```{figure} discord_set_oath_permissions.png
---
name: discord_set_oath_permissions_fig
alt: "Screenshot of discord developer application screen with OAuth2 General tab selected. In the Scopes section, both \"bot\" and \"applications.commands\" options selected. In the Bot Permissions section, under \"General Permissions\" one option is selected: \"Read Messages/View Channels\", under \"Text Permissions\" all options are selected except for \"Use Embedded Activities\", and under \"Voice Permissions\" no options are selected."
---
A starting set of permissions for your bot.
```

Now go to URL Generator to create an invite link for your bot. You'll get a permission set of options again, where we've chosen the same permissions as before. At the very bottom there is an option to copy a the url, which is an invite link to your bot. Copy this and save it. 
```{figure} discord_generate_url.png
---
name: discord_generate_url_fig
width: 500px
alt: "Screenshot of discord developer application screen with OAuth2 General tab selected. In the Scopes section, only the \"bot\" options is selected. In the Bot Permissions section, the same permissions are selected as in the previous screenshot. At the very bottom there is a Generated URL with a \"Copy\" button, which is circled."
---
Copy the invite link (use same permissions as before).
```

This invite link can be given to the owner of any discord server and they can use it to invite your bot to their server.

## Add app to a Discord Server
To add your bot to your own discord server, open a new browser tab and copy the link in to the url bar. Then you will have an option to add your bot to any servers you own.

```{figure} discord_add_app_to_server.png
---
name: discord_add_app_to_server_fig
width: 400px
alt: "A new browser tab is opened with the Generated URL copied into it. This opens a site saying \"An external application wants to access your Discord account.\" The \"Add To Server\" section is highlighted with a Discord server selected, and the \"Continue\" button is circled."
---
Add your bot to one of your servers.
```

Note: After adding app to server, there is a confirmation page about the permissions. "Authorize" your bot.

## Get Channel Id Number

One additional piece of information you might need for your bot is the channel ID for a channel in a discord server. In order to get a channel ID, open your settings menu.

```{figure} discord_enable_dev_mode_1.png
---
name: discord_enable_dev_mode_1_fig
width: 300px
alt: "The discord profile part of the screen with the username, and mute options. The gear options button is circled."
---
Open your settings menu.
```

Then enable developer mode in the advanced settings.
```{figure} discord_enable_dev_mode_2.png
---
name: discord_enable_dev_mode_2_fig
width: 500px
alt: "In the discord settings change, the advanced tab is selected. In the advanced tab \"Developer mode\" is circled to turn on."
---
Enable developer mode.
```

Once developer mode is on, you can get a channel ID by right-clicking on a channel.
```{figure} discord_get_channel_id.png
---
name: discord_get_channel_id_fig
width: 400px
alt: "A screenshot of a discord server page. One of the channels has been right-clicked on, and the very bottom of the right-click menu is the \"Copy Channel ID\" option, which is circled."
---
Copy the channel ID by right clicking.
```

Save the channel ID somewhere so you can have your bot reference it later (e.g., post to that channel).

##  Test your tokens
Now that you have your token, and other info, you can test out your code in chapter 2.3.8 ([](../../ch02_definitions/03_automation/08_demo.ipynb)). You can try running the code and replacing the fake discord token and channel ids with the ones from your account, and see if you can use the code to make an actual post to your account.

## Understand Discord Rules for Bots
Before you try doing anything too creative with Discord bots, make sure you look over the [Discord Developer Policy](https://discord.com/developers/docs/policies-and-agreements/developer-policy), that way you don't get yourself banned.