# Data in a Social Media Post

Let's look at all the data that we can see when we look at a tweet on what was Twitter:
```{figure} dog_tweet.png
---
name: tweet_example_fig
alt: Screenshot of tweet from user WeRateDogs® (@dog_rates). Tweet text is "This is Woods. He’s here to help with the dishes. Specifically the pre-rinse, where he licks every item he can. 12/10". The tweet also has three photos of a tiny cute puppy standing on the open door of a dishwasher. The tweet was posted on Feb 10, 2020. The account that posted it has a blue check. The tweet has 1,533 quote tweets, 26.6K retweets, and 197.8K likes.
---
A tweet with photos of a cute puppy! ([source](https://twitter.com/dog_rates/status/1227037345712627718))
```

In this screenshot of Twitter, we can see the following information:
- The account that posted it:
  - User handle is @dog_rates
  - User name is WeRateDogs®
  - User profile picture is a circular photo of a white dog
  - This user has a blue checkmark
- The date of the tweet: Feb 10, 2020
- The text of the tweet: "This is Woods. He’s here to help with the dishes. Specifically, the pre-rinse, where he licks every item he can. 12/10"
- The photos in the tweet: Three photos of a puppy on a dishwasher
- The number of replies: 1,533
- The number of retweets: 26.2K
- The number of likes: 197.8K

## Data and Metadata

One way we can categorize the data in this tweet is to separate it into data and metadata, like this:

```{figure} dog_tweet_metadata.png
---
name: tweet_metadata_fig
alt: 'Screenshot of the tweet above, but with a box around the tweet text and photos labeled "Data (Tweet Contents)
", and the rest of the information outside the box is labeled "Metadata (Data About Tweet)"'
---
The "data" of a tweet consists of the tweet text and the photos. The "metadata" of a tweet is all the rest of the information about that tweet, such as who tweeted it, and when, and how people responded.
```

__Metadata__ is information about some data. So we often think about a dataset as consisting of the main pieces of data (whatever those are in a specific situation), and whatever other information we have about that data (metadata).

For example:
- If we think of a tweet's contents (text and photos) as the main data of a tweet, then additional information such as the user, time, and responses would be considered metadata.
- If we download information about a set of tweets (text, user, time, etc.) to analyze later, we might consider that set of information as the main data, and our metadata might be information about our download process, such as when we collected the tweet information, which search term we used to find it, etc.

% TODO: Another metadata example: tweet search, the results are data, the search string and time are metadata

% TODO: Define a database

Now that we've looked some at the data in a tweet, let's look next at how different pieces of this information are saved.
