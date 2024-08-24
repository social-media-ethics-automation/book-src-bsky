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

_Note: Instructions are based on the official instructions here: [https://discord.com/developers/docs/getting-started](https://discord.com/developers/docs/getting-started)_

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


To do this, go to the installation tab where you will be able to get an invite link.

```{figure} discord_install_tab.png
---
name: discord_install_tab_fig
alt: "Screenshot of discord developer application screen with the Install tab selected."
---
Select the install tab
```


 For this textbook, we suggest only using "Guild Install," then scroll down and set default scopes to:
- application.commands
- bot

We then suggest the following permissions:
- Attach Files
- Create Public Threads
- Read Message History
- Send Messages
- Send Messages in Threads
- View Channels

```{figure} discord_set_permissions.png
---
name: discord_set_permissions_fig
alt: "In the Install tab, under 'select methods' only 'Guild Install' is selected. Then below in 'Default Install Settings' under 'Guild Install' the scopes selected are 'application.commands' and 'bot'. Under permissions are 'Attach Files', 'Create Public Threads', 'Read Message History', Send Messages', 'Send Messages in Threads' and 'View Channels'."
---
Set default permissions
```

_Note: We are new to Discord bots and don't know the permission structure wells. If you are looking at doing more with your bots, you can see more about [the different permissions here](https://discord.com/developers/docs/topics/oauth2#shared-resources-oauth2-scopes), and in particular we recommend looking into adding [application commands](https://discord.com/developers/docs/interactions/application-commands)._


Make sure to save changes!

Then you can copy the Install Link

```{figure} discord_copy_link.png
---
name: discord_copy_link_fig
alt: "In the Install tab, under 'install link' is the 'Discord Provided Link', with 'copy' highlighted."
---
Copy the install link
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

## Get Channel Id and Server Id Numbers

Two additional pieces of information you might need for your bot ares the channel ID for a channel in a discord server, and the server ID (or "Guild Id") for the server itself. In order to get the channel IDs, and server IDs, open your settings menu.

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

You can also get the server ID (or "Guild ID") by right-clicking on a channel.
```{figure} discord_copy_server_id.png
---
name: discord_copy_server_id_fig
width: 400px
alt: "A screenshot of a discord server page. One of the servers has been right-clicked on, and the very bottom of the right-click menu is the \"Copy Server ID\" option, which is circled."
---
Copy the server ID by right clicking.
```

Save the channel IDs and server IDs somewhere so you can have your bot reference it later (e.g., post to that channel).

##  Test your tokens
Now that you have your token, and other info, you can test out your code in chapter 2.3.8 ([](../../ch02_definitions/03_automation/08_demo.ipynb)). You can try running the code and replacing the fake discord token and channel ids with the ones from your account, and see if you can use the code to make an actual post to your account.

## Understand Discord Rules for Bots
Before you try doing anything too creative with Discord bots, make sure you look over the [Discord Developer Policy](https://discord.com/developers/docs/policies-and-agreements/developer-policy), that way you don't get yourself banned.