# What Recommendation Algorithms Do

When social media platforms show users a series of posts, updates, friend suggestions, ads, or anything really, they have to use some method of determining which things to show users. The method of determining what is shown to users is called a __recommendation algorithm__, which is an algorithm (a series of steps or rules, such as in a computer program) that recommends posts for users to see, people for users to follow, ads for users to view, or reminders for users.

Some recommendation algorithms can be simple such as reverse chronological order, meaning it shows users the latest posts (like how blogs work, or Twitter's "See latest tweets" option). They can also be very complicated taking into account many factors, such as:
- Time since posting (e.g., show newer posts, or remind me of posts that were made 5 years ago today)
- Whether the post was made or liked by my friends or people I'm following
- How much this post has been liked, interacted with, or hovered over
- Which other posts I've been liking, interacting with, or hovering over
- What people connected to me or similar to me have been liking, interacting with, or hovering over
- What people near you have been liking, interacting with, or hovering over (they can find your approximate location, like your city, from your internet IP address, and they may know even more precisely)
  - This perhaps explains why sometimes when you talk about something out loud it gets recommended to you (because someone around you then searched for it). Or maybe they are actually recording what you are saying and recommending based on that.
- Phone numbers or email addresses ([sometimes collected deceptively](https://techcrunch.com/2019/03/03/facebook-phone-number-look-up/) {cite:p}`whittakerFacebookWonLet2019`) can be used to suggest friends or contacts.
- And probably many more factors as well!

Now, how these algorithms precisely work is hard to know, because social media sites keep these algorithms secret, probably for multiple reasons:
- They don't want another social media site copying their hard work in coming up with an algorithm
- They don't want users to see the algorithm and then be able to complain about specific details
- They don't want malicious users to see the algorithm and figure out how to best make their content go viral


## Choosing Recommendation Algorithms
Sometimes social media platforms let users choose between different recommendation algorithms, like in the examples below:


```{figure} reddit_recommendation_options.png
---
width: 150px
name: reddit_recommendation_options_fig
alt: "Reddit dropdown menu for \"sort by\" with options: hot, new, top, rising"
---
Reddit subreddit options for sort order of posts (according to different algorithms).
```

```{figure} pandora_recommendation_options.png
---
width: 400px
name: pandora_recommendation_options_fig
alt: "Pandora menu for \"choose a mode to fine-tune your station\" with options: My station, Crowd Faves, Discover, Deep Cuts, Newly Released, Artist Only"
---
Pandora music app recommendation options.
```


## Reflections
- What experiences do you have of social media sites making particularly good recommendations for you?
- What experiences do you have of social media sites making particularly bad recommendations for you?

