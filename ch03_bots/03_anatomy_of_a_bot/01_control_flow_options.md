# Organizing a Computer Program

In order to understand how a bot is built and can work, we will now look at the different ways computer programs can be organized. We will cover a bunch of examples quickly here, to hopefully give you an idea of many options for how to write a program. Don't worry if you don't follow all of it, as we will go back over these one at a time in more detail throughout the book.

In this section, we will not show actual Python computer programs (that will be in the next section). Instead, here we will focus on what programmers call "[psuedocode](https://en.wikipedia.org/wiki/Pseudocode) {cite:p}`Pseudocode2023`," which is a human language outline of a program. Psuedocode is intended to be easier to read and write. Pseudocode is often used by programmers to plan how they want their programs to work, and once the programmer is somewhat confident in their pseudocode, they will then try to write it in actual programming language code.

```{note}
The programs outlined below in pseudocode are meant to demonstrate what could be done with a computer program, not what should be done or what would necessarily be a good idea.
```

## Statements: Steps that Run In Order
Python is in a group of programming languages called [imperative programming languages](https://en.wikipedia.org/wiki/Imperative_programming) {cite:p}`ImperativeProgramming2023`[^language_types_footnote]. At their core, programs written in imperative programming languages consist of a list of "statements" to be run in order.

[^language_types_footnote]: There are other types of programming organizations as well, such as [functional programming](https://en.wikipedia.org/wiki/Functional_programming) {cite:p}`FunctionalProgramming2023` (like [Excel](https://www.microsoft.com/en-us/research/blog/lambda-the-ultimatae-excel-worksheet-function/) {cite:p}`hagenEnrichingExcelHigherorder2021` and [Google Sheets](https://www.google.com/sheets/about/) {cite:p}`GoogleSheetsOnline`),  [visual programming](https://en.wikipedia.org/wiki/Visual_programming_language) {cite:p}`VisualProgrammingLanguage2023` (like the educational [Scratch](https://scratch.mit.edu/) {cite:p}`ScratchImagineProgram`, or the 3D Graphics [Blender node editor](https://docs.blender.org/manual/en/2.79/editors/node_editor/introduction.html]) {cite:p}`IntroductionBlenderManual`), [declarative programming](https://en.wikipedia.org/wiki/Declarative_programming) {cite:p}`DeclarativeProgramming2023` (like HTML and CSS web content) [object oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming) {cite:p}`ObjectorientedProgramming2023` (can be done in Python, JavaScript, and many others), and [many more](https://en.wikipedia.org/wiki/Programming_paradigm) {cite:p}`ProgrammingParadigm2023`.

So a program in one of these languages would look like:
```text
- statement 1
- statement 2
- statement 3
```
And when the program is run, statement 1 runs first, then statement 2, then, finally, statement 3.

You might recognize this as the same style of instructions as a cooking recipe, like making dumplings:
```text
- Make dumpling dough.
- Make veggie filling.
- Flatten small balls of dough.
- Put some filling on each piece of dough.
- Fold dough around the filling.
- Steam the dumplings.
```

In fact, the format of a cooking recipe is basically an imperative programming language where the cook acts as a "human computer" following the cooking instructions.

> ![Photo of a man in a kitchen, looking at a notebook while mixing something in a bowl. The bowl is surrounded by eggs, strawberries and other ingredients.](cooking.jpg)
> A human computer running a cooking program. In other words: "someone following a recipe" (but probably not a dumpling recipe) ([photo source](https://www.pexels.com/photo/a-man-cooking-at-the-kitchen-6944110/) {cite:p}`PhotoVladaKarpovich`)

Social Media bots are generally organized in this same way, so one bot might be organized like this:
```text
- Log into the social media app
- Find any new posts that mention me that also have curse words
- Look up the users who posted those tweets
- Block those users
```

````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Also, you'll notice that the actual code has a lot more steps then our psuedocode above has.

Note: This code is untested and we may have made programming errors, and Twitter (now called "X") doesn't allow free bot accounts anymore.
```python

########  Log Into Twitter  #######

import tweepy

# Load all your developer access passwords into Python
# TODO: Put your twitter account's special developer access passwords below:
bearer_token = "n4tossfgsafs_fake_bearer_token_isa53#$%$"
consumer_key = "sa@#4@fdfdsa_fake_consumer_key_$%DSG#%DG"
consumer_secret = "45adf$T$A_fake_consumer_secret_JESdsg"
access_token = "56sd5Ss4tsea_fake_access_token_%YE%hDsdr"
access_token_secret = "j^$dr_fake_consumer_key_^A5s#DR5s"

# Give the tweepy code your developer access passwords so
# it can perform twitter actions
client = tweepy.Client(
   bearer_token=bearer_token,
   consumer_key=consumer_key, consumer_secret=consumer_secret,
   access_token=access_token, access_token_secret=access_token_secret
)


########  Find any new tweets that mention me that also have curse words  #######

# get my twitter id
my_info = client.get_user(id = "me", user_auth = True)
my_id = my_info.data.id

# get all tweets that mention me
mentions = client.get_users_mentions(id = my_id)

# import profanity checking library
from profanity_check import predict

# start a list of mentions that have curse words
cursing_mentions = []

# Go through the tweets to see which ones have curse words
for mention in mentions.data:
    # check if the tweet has a curse word
    if(predict(mention.text))[0] == 1):
       # if it did have a curse word, put it in the cursing mentions list
       cursing_mentions.append(mention)


########  Look up the users who posted those tweets  ########

# start a list of users to block (starts out empty)
users_to_block = []

# Go through each cursing mention tweet
for cursing_mention in cursing_mentions:
    # look up the user id for each cursing tweet, and add it to the list of users to block
    users_to_block.append(tweet.author_id)


########  Block those users  ########

# Go through each of the users to block
for user_to_block in users_to_block:
    # block the user
    client.block(target_user_id)
```
````

We will show how to use statements in Python in the next section of this chapter: ([](02_demo_statements_variables_sleep.ipynb)).

## Variables: Save information for later
Variables are a way of saving information on the computer, so we can use it later in the computer program.

In a cooking recipe, the equivalent would be spaces, containers, bowls, or cups to hold ingredients. So you might place the ingredients on the counter in preparation for cooking. Or you might combine some ingredients in a mixing bowl, so the mixing bowl holds the combined ingredients through each step, like:
```text
To make the dumpling dough:
- Put flour in a mixing bowl and add a bit of salt
- Make a well in the middle of the flour
- Crack the egg into the well (discarding the shell) and use your fingertips to gradually incorporate the flour
- Bring together and knead for about 10 minutes until smooth and elastic, rather than rough and floury.
- Wrap in clingfilm and rest it in the fridge for at least 30 minutes.
```

Sometimes in cooking, you use multiple mixing bowls to mix different parts of the recipe separately:
```text
To make the dumpling filling:
- While the dough is chilling, In a separate mixing bowl:
  - Combine the sauteed onions, pumpkin, and mushrooms
  - Add a generous handful of finely chopped fresh dill and parsley
  - Mix to combine, then taste. If it needs more salt, add more salt. If it needs some brightness, add a small amount for lemon juice or white rice vinegar, then taste it again.
```

In a computer program, when you save information for later use, instead of putting it in a bowl, you give it a name. The computer then makes a place in its memory with that name, and saves the information you asked it to save. Then you can use that name later in the program to ask the computer what was saved in that spot.

For example, I might save my first and last name separately in the computer, then combine them together to make my full name (which I save), and then use that full name to send a private message to introduce myself:
```text
- Save my first name in a variable called "first_name"
- Save my last name in a variable called "last_name"
- Create the text of my full name by combining what is in the variable "first_name",
  followed by a space, followed by what is in the variable "last_name", then save
  it in a new variable called "full_name"
- Post a tweet saying "Hello my name is ___" but filling in the blank
  with what is in the variable "full_name"
```
````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

first_name = "Kyle"
last_name = "Thayer"
full_name = first_name + " " + full_name

client.create_tweet(text="Hello my name is " + full_name)
```
````


Or, when I am looking something up, like my latest tweets, I can save that in a variable so I can look up replies to those tweets the next step:
```text
- Find my latest tweet, and save it as a variable named "my_latest_tweet"
- Search for all tweets that are in the same conversation as my latest tweet, and save them in the variable "my_latest_tweet_replies"
```

````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

# get my twitter id
my_info = client.get_user(id = "me", user_auth = True)
my_id = my_info.data.id

# Get my latest tweet (and get the conversation id for that tweet)
my_latest_tweet = client.get_users_tweets(my_id,  tweet_fields=['conversation_id'])[0]

# Search for tweets that are in the same conversation as my latest tweet
my_latest_tweet_conversation = client.Client.search_recent_tweets("conversation_id:" + str(my_latest_tweet.data.conversation_id))
```
````

We will show how to use variables in Python in the next section ([](02_demo_statements_variables_sleep.ipynb)).


## Events: When you do something depends
Events let us perform a programming action in response to something happening. The computer may sit and do nothing while waiting for an event to happen.

Within cooking this might look like:
```text
- When the guests arrive, boil or steam the dumplings, and then plate and serve them.
```

Within programming, it might look like:
```text
- Whenever someone tags me in a post
  - like their post which has me tagged
```


````{admonition} Click to see a note on Python
:class: dropdown
Note: Python isn't by default set up with event style programming. We won't be directly doing event programming in this book.

We will be doing the Pausing/Scheduling below, which you can use to do some of the same things (e.g., check in every five minutes to see if there are new tweets that tag me).
````


### Pausing/Scheduling
One of the most common events to program for is around time: We can also tell programs to wait for a period of time, or start at a given time.

In cooking this might look like:
```text
- Boil the dumplings for 5 minutes
```

or
```text
- Start the process of making dumplings 2 hours before guests arrive.
```


In programming, it might look like:
```text
- Post this set of tweets, pausing 30 seconds between each tweet
```

````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

# load a library that gives us a pause action (called sleep)
import time

# post a tweet
client.create_tweet(text="I am a bot pretending to slowly type in a series of tweets.")

# pause for 30 seconds
time.sleep(30)

# post a tweet
client.create_tweet(text="This is my second tweet.")

# pause for 30 seconds
time.sleep(30)

# post a tweet
client.create_tweet(text="It takes a little while for me to pretend to type up each of these tweets")

# pause for 30 seconds
time.sleep(30)

client.create_tweet(text="here is my final tweet")

```
````

Or

```text
- every day at noon, post a tweet saying "It's lunchtime!"
```

````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

# load a library that gives us a scheduling actions
import schedule

# Define a function that when run will say that it is lunchtime
def say_it_is_lunchtime():
    # when the function is run, post a tweet
    client.create_tweet(text="It's lunchtime!")


# schedule the "say_it_is_lunchtime" function to run every day at noon
schedule.every().day.at("12:00").do(say_it_is_lunchtime)


# Loop forever, once a second running every task that needs to be run
while True:
    # if any tasks are ready to run, run them
    schedule.run_pending()
    # pause for 1 second before checking again
    time.sleep(1)

```
````


We will show how to use pausing in the next section ([](02_demo_statements_variables_sleep.ipynb)).

We will show how to use other Events and Scheduling in Python in Chapter 18: Public Shaming.


## Conditionals: What you do depends
Conditionals let us change what we do depending on the situation.

In cooking, we might taste for seasoning and change our course of action depending on that test:
```text
- Taste the filling.
  - If it is good, proceed to the next section.
  - Otherwise (if it is not quite right)
    - If it needs more salt, add more salt
    - If it needs some brightness, add a small amount for lemon juice or white rice vinegar
```

In programming, we might do this:
```text
- look up the latest tweet mentioning me
  - if that tweet says "It's time to go", then post "Let's go!"
  - otherwise, post "I am still waiting"
```


````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

# get my twitter id
my_info = client.get_user(id = "me", user_auth = True)
my_id = my_info.data.id

# get the latest tweet that mentions me
latest_mention = client.get_users_mentions(id = my_id).data[0]

if "It's time to go" in latest_mention.text:
   client.create_tweet(text="Let's go!")
else:
   client.create_tweet(text="I am still waiting")

```
````

We will show how to use conditionals in Chapter 7: Trolling.


## Loops: Repeating Actions
Loops are used to repeat actions, though there are several different types of repetitive actions.

In cooking you can repeat an action a set number of times:
```text
- Cut the dough 19 times to make 20 (6 cm) squares.
```

Or you can repeat the same action, but to different items:
```text
- For each square of dumpling dough
  - fill them with dumpling filling and bring up the corners. Pinch together the edges to seal.
```

Or you can repeat the same action until you get a certain result:
```text
- Continue kneading the dough until it is smooth and elastic, not rough and floury.
```

In computer programming, you can repeat an action a set number of times

<pre>
- Tweet this 100 times: "Warner Brothers should <a href="https://www.rollingstone.com/tv-movies/tv-movie-features/justice-league-the-snyder-cut-bots-fans-1384231/">#ReleaseTheSnyderCut</a> of the Justice League movie."
</pre>

````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

If you try this yourself, it wont post 100 times, since the twitter blocks you from repeating the same exact tweet repeatedly.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

# repeat this action 100 times
for i in range(100):
    # post a tweet
    client.create_tweet(text="Warner Brothers should #ReleaseTheSnyderCut of the Justice League movie.")

```
````

Or a computer program can repeat an action to a set of items

```text
- Like each of the tweets that were in the same conversation as my latest tweet
```

````{admonition} Click to see actual code
:class: dropdown
You are not expected to understand all this code. It is here to give you an examples of what code looks like.

Note: This code is untested and we may have made programming errors
```python
# TODO: Copy tweepy and login steps here

# Get my latest tweet (and get the conversation id for that tweet)
my_latest_tweet = client.get_users_tweets(my_id,  tweet_fields=['conversation_id'])[0]

# Search for tweets that are in the same conversation as my latest tweet
my_latest_tweet_conversation = client.Client.search_recent_tweets("conversation_id:" + str(my_latest_tweet.data.conversation_id))

# repeat this action for all the tweets in the conversation
for tweet in my_latest_tweet_conversation.data:
    # like the tweet
    client.like(tweet.id)

```
````



Or a computer program can repeat an action until a condition is met:
```text
- Keep sending private messages to this person until they say "Stop it!"
```

````{admonition} Click to see a note
:class: dropdown
Note: I am not going to directly give you code for harassing someone.

As for repeating an action until a condition is met, those are done with [while loops](https://www.w3schools.com/python/python_while_loops.asp) {cite:p}`PythonLoops`. Feel free to use while loops when you have a legitimate, non-harassment use.
````

We will show how to use loops in Chapter 5: History of Social Media.

## Code Blocks: Grouping statements
Sometimes in programming, we want to group several steps (i.e., statements) together. When we group these steps together we call it a code "block." These blocks of code often used with conditionals (e.g., if this condition is true, do these five steps), and with loops (e.g., for each of these items, do these five steps).

In a recipe, you might create a block of instructions like this:
```text
- for each of the squares of dumpling dough:
  - place one spoonful of filling in the middle of the square
  - fold the dough over the filling
  - pinch the edges to seal it
  - set the dumpling on a piece of parchment paper to await cooking
```

In a computer program, you might make a code block of statements like this:

```text
- for each of the latest tweets that mention me:
  - look up the time of the tweet (in your time zone)
  - look up the location the tweet was posted in
  - calculate the local time of the person tweeting when they tweeted
  - reply to their tweet ("you posted that tweet at ___ in your time zone")
```

Using code blocks allows you to do things like put conditionals inside of loops
```text
- for each of the latest tweets that mention me:
  - look up if the tweet was posted from android or an iPhone
    - if it was from an android, like the tweet
    - if it was from an iPhone, block the user who made the tweet
```


We will show how to use code blocks in Chapter 5: History of Social Media.

## Functions/Libraries: Run another program
The final programming organization feature we will cover here is functions and libraries, which basically allow you to run another computer program. This could be a small program that you made that want to use, or it could be a program written by someone else that you are using.

In cooking, this might look like a step of asking the cook to make something from another recipe.
```text
- Make the dumpling dough (see recipe on page 42).
```

The recipe also could ask you to make a different version of a recipe from another page:
```text
- to make dumplings vegan, make the dumpling
  dough (see recipe on page 42), but instead of using the egg, subsititute 2 teaspoons olive oil and 2 tablespoons hot water.
```

In programming, a function is a small program that you can run from another place in the code (programmer call this "calling" a function). Functions also can accept data and options for how they run. Code libraries are a collection of functions and data that help with certain tasks.

In this book, we will be using the [praw](https://praw.readthedocs.io/) {cite:p}`PRAWDocumentationa` code library, which comes with many pre-written functions that help us do actions on Reddit, functions like:
- `subreddit` (to select a subreddit)
- `submit` (to submit to a subreddit)
- `submit_image` (to submit an image to a subreddit)
- `top` (to get the current top posts off a subreddit)
- `upvote` (to upvote a post or comment)
- etc.[^praw_functions_footnote]

[^praw_functions_footnote]: You can get a full list of praw functions by starting from [this Praw documentation page](https://praw.readthedocs.io/en/latest/code_overview/praw_models.html) {cite:p}`WorkingPRAWModels`. That page has links for each type of thing on reddit, such as a comment, redditor, submission, etc. If you follow one of those you will get information on the different things you can do with those on using praw. Unfortunately, it is not easy to read this information, but we will cover pieces of it as w ego in this book.

If you look back over the various psuedocode and code examples above, most of them involve calling various functions, (though those examples use the tweepy library for Twitter). Additionally, the scheduling example code includes defining a new function and using it.

We will show examples of calling functions starting in the next section.

We will show how to write functions in Chapter 9 (Privacy and Security).
