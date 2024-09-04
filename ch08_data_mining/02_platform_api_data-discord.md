# Data From the Discord API

When we've been accessing Discord through Python and the "discord" code library. The discord code library works by sending requests across the internet to Discord, using what is called an "[application programming interface](https://en.wikipedia.org/wiki/API)" {cite:p}`API2023a` or API for short. APIs have a set of rules for what requests you can make, what happens when you make the request, and what information you can get back.

If you are interested in learning more about what you can do with praw and what information you can get back, you can look at the official documentation for those. But be warned they are not organized in a friendly way for newcomers and take some getting used to to figure out what these documentation pages are talking about.

So, if you are interested, you can look at [the discord library documentation](https://discordpy.readthedocs.io/en/stable/) {cite:p}`noauthor_welcome_nodate` to find out what the library can do (again, not organized in a beginner-friendly way). You can learn a little more by searching the api docs for things like the [discord.Message](https://discordpy.readthedocs.io/en/stable/api.html#discord.Message) {cite:p}`noauthor_api_nodate` and finding a list data ("attributes") and functions ("Methods") for that piece of discord.


Also, for slash commands, we use the [iteractions.py](https://interactions-py.github.io/interactions.py/) {cite:p}`noauthor_interactionspy_nodate` code library. You can see [guides on how to use it here](https://interactions-py.github.io/interactions.py/Guides/) {cite:p}`noauthor_guides_nodate`.

The discord API lets you access just some of the data that Discord tracks, but Discord and other social media platforms track much more than they let you have access to.
