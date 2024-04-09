# Making a Bot Account (Reddit)



In using this textbook, you will have opportunities to create and run social media bots. Here we will run through how to create a Reddit account and set it up for running your own bots.

While we have made a fake version of Reddit for you to test all the code in this book, we highly encourage you to make a reddit bot account and try it out for real!

## Sign up for Reddit
[https://www.reddit.com/register/](https://www.reddit.com/register/)

We suggest making a new, separate Reddit account, just for making reddit bots, since you don't want to accidentally get your main reddit account banned or labeled as a bot.

Note: If you want to make a new account and you already have one, you may need to sign out from your current account, or use a different web browser (e.g., Mozilla, Google Chrome, Microsoft Edge, Safari).

## Create Reddit bot "application"

Once you are logged into Reddit, go to user settings:

```{figure} reddit_user_settings.png
---
name: reddit_user_settings_fig
width: 200px
alt: "Screenshot of the user menu at the top right of the screen, with 'User Settings' highlighted."
---
```

In the user settings, go to the Safety & Privacy tab and click the Manage third-party app authorization link at the bottom. This should take you to an apps tab (you can also try going straight there [with this link](https://www.reddit.com/prefs/apps)). Click on the bottom button that says "are you a developer? create an app..."

```{figure} reddit_create_app_button.png
---
name: reddit_create_app_button_fig
width: 400px
alt: "screenshot of the user settings (called 'preferences' on this page) with the apps tab selected. There is a list of auhtorized apps, with reddit on mobile web as the first one, and then a button at the bottom which we have highlighted called 'are you a developer? create an app...'"
---
```


Once you are on the create application page, make up a name for your bot (I chose "class_testing_scripts"), then choose the "scripts" type, fill in a description, and for the redirect uri, use "http://www.example.com/unused/redirect/uri"
```{figure} reddit_create_app_form.png
---
name: reddit_create_app_form_fig
width: 500px
alt: "Screeshot of create application page with name as 'class_testing_scripts'; then type set to 'script' (instead of web app or installed app); then description filled out as 'This will be used to learn how to program with Reddit as part of a class'; then about url left blank, and redirect url as 'http://www.example.com/unused/redirect/uri'"
---
```

Once you are done, you should see the app information, which includes two key values: the client_id and the client_secret. Copy these so that you can use them later to run your bot.

```{figure} reddit_bot_keys.png
---
name: reddit_bot_keys_fig
width: 500px
alt: "Screenshot of the app information. Under the name and description of the app is the client_id, which is a bunch of random numbers and letters (though I blocked it out in the screenshot). Below that is the 'secret', another set of random numbers and letters, which I blocked out as well."
---
```


##  Test your keys
Now that you have your keys, and other info, you can test out your code in chapter 2.3.8 ([](../../ch02_definitions/03_automation/08_demo.ipynb)), you can try running the code and replacing the fake special passwords with the ones from your account, and see if you can use the code to post an actual tweet to your account.

## Understand Reddit Rules for Bots
Before you try doing anything too creative with reddit  bots, make sure you look over the [Reddit API Terms of Use](https://docs.google.com/forms/d/e/1FAIpQLSezNdDNK1-P8mspSbmtC2r86Ee9ZRbC66u929cG2GX0T9UMyw/viewform) and the [Reddit API Rules](https://github.com/reddit-archive/reddit/wiki/API#rules), that way you don't get yourself banned.
