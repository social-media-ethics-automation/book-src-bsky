# Grouping data

Once we have some types of data representation on a computer, we can create different groupings of data to represent more types of data. We'll look at two types of groupings here: Lists and Dictionaries.

## Lists
The first way of combining data is by making a list.

So we can make a list of the numbers from 1 to 10:
 - 1, 2, 3, 4, 5, 6, 7, 8, 9, 10

 ````{admonition} Click to see example Python code
 :class: dropdown
 ```python
 # Save a list of the numbers from 1 to 10 in a variable called one_to_ten
 one_to_ten = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
 ```
 ````

In our example tweet we can see several places where data could be saved in lists:

 ```{figure} dog_tweet_with_lists.png
 ---
 name: tweet_lists_fig
 alt: "Screenshot of the tweet from before, but with lists highlighted: images, and links to the lists of replies, retweets, and likes."
 ---
 There are several lists in the tweet. There is a list of three images, and there are links that will take you to the lists of replies, retweets, and likes.
 ```

 ````{admonition} Click to see example Python code
 :class: dropdown
 ```python
 # Save a list of people who liked a tweet in a variable called tweet_likes
 tweet_likes = ["@kylemthayer", "@SusanNotess"]
 ```
 ````

Additionally the text strings we saw before are actually stored internally as lists of characters.


The items in lists are normally numbered with an "index", so you can ask for the 1st item, or 2nd item, or any other.

Note: Largely due to [historical peculiarities in the development of programming languages](https://en.wikipedia.org/wiki/Zero-based_numbering#Origin) {cite:p}`ZerobasedNumbering2023`, most programming languages (including Python) number the 1st item in a list as item "0". So:
- 1st item has index 0
- 2nd item has index 1
- 3rd item has index 2
- etc.

````{admonition} Click to see example Python code
:class: dropdown
```python

# Save a list of twitter handles in a list called book_authors
book_authors = ["@kylemthayer", "@SusanNotess"]

# Save the first author twitter handle in a variable called first_author
first_author = book_authors[0]

# Save the second author twitter handle in a variable called second_author
second_author = book_authors[1]


# Save a string (a list of characters) in a variable called key_word
key_word = "ethics"

# Get the first letter ("e"), and save it in variable first_letter
first_letter = key_word[0]

Get the second letter ("t"), and save it in variable second_letter
second_letter = key_word[1]
```
````

There are many types of list data structures in different programming languages with subtle differences (we won't worry about those in this book). Python has [lists](https://www.w3schools.com/python/python_lists.asp) {cite:p}`PythonLists`, [tuples](https://www.w3schools.com/python/python_tuples.asp) {cite:p}`PythonTuples`, and [sets](https://www.w3schools.com/python/python_sets.asp) {cite:p}`PythonSets`. Other languages have a list type called [arrays](https://en.wikipedia.org/wiki/Array_data_type) {cite:p}`ArrayDataType2023`. We will just focus on lists and not worry about the other similar data types.

We'll demonstrate lists later in Chapter 5: History of Social Media.

## Dictionaries
The other method of grouping data that we will discuss here is called a "dictionary" (sometimes also called a "map").

You can think of this as like a language dictionary where there is a word and a definition for each word. Then you can look up any name or word and find the value or definition.

Example: An English Language Dictionary with definitions of three terms:
- __Social Media__: An internet-based platform used for people to form connections to each other and share things.
- __Ethics__: Thinking systematically about what makes something morally right or wrong, or using ethical systems to analyze moral concerns in different situations
- __Automation__: Making a process or activity that can run on its own without needing a human to guide it.

The Dictionary data type allows programmers to combine several pieces of data by naming each piece. When we do this, the dictionary will have a number of names, and for each of those names a piece of information (called a "value" in this context).

Dictionary:
- Name 1: Value 1
- Name 2: Value 2
- Name 3: Value 3

So if we look at the example tweet, we can combine all the data in a dictionary.
```{figure} dog_tweet.png
---
name: tweet_dictionary_fig
alt: Screenshot of tweet from user WeRateDogs® (@dog_rates). Tweet text is "This is Woods. He’s here to help with the dishes. Specifically the pre-rinse, where he licks every item he can. 12/10". The tweet also has three photos of a tiny cute puppy standing on the open door of a dishwasher. The tweet was posted on Feb 10, 2020. The account that posted it has a blue check. The tweet has 1,533 quote tweets, 26.6K retweets, and 197.8K likes.
---
A tweet with photos of a cute puppy! ([source](https://twitter.com/dog_rates/status/1227037345712627718))
```

Dictionary (with some of the data):
 - user_name: "WeRateDogs®"
 - user_handle: "@dog_rates"
 - user_has_blue_checkmark: True
 - tweet_text: "This is Woods. He’s here to help with the dishes. Specifically the pre-rinse, where he licks every item he can. 12/10"
 - number_of_replies: 1533
 - number_of_retweets: 26200
 - number_of_likes: 197800

 ````{admonition} Click to see example Python code
 :class: dropdown
 ```python
 # Save some info about a tweet in a variable called tweet_info
 tweet_info = {
  "user_name": "WeRateDogs®",
  "user_handle": "@dog_rates",
  "user_has_blue_checkmark": True,
  "tweet_text": "This is Woods. He’s here to help with the dishes. Specifically the pre-rinse, where he licks every item he can. 12/10",
  "number_of_replies": 1533,
  "number_of_retweets": 26200,
  "number_of_likes": 197800
}
 ```
 ````


Note: We'll demonstrate dictionaries later in Chapter 5: History of Social Media, and Chapter 8: Data Mining.


## Groups within Groups
We can use dictionaries and lists together to make lists of dictionaries, lists of lists, dictionaries of lists, or any other combination.

So for example, I could make a list of Twitter users. Each Twitter user could be a dictionary with info about that user, and one piece of information it might have is a list of who that user is following.

List of users:

User 1:
- Username: kylethayer (a String)
- Twitter handle: @kylemthayer (a String)
- Profile Picture: [TODO picture here] (an image)
- Follows: @SusanNotess, @UW, @UW_iSchool, @ajlunited, ... (a list of Strings)

User 2:
- Username: Dr Susan Notess (a String)
- Twitter handle: @SusanNotess (a String)
- Profile Picture: [TODO picture here] (an image)
- Follows: @kylemthayer, @histoftech, @j_kalla, @dbroockman, @qaxaawut, @shengokai, @laniwhatison (a list of Strings)


````{admonition} Click to see example Python code
:class: dropdown
```python
users = [
  {
    username: "kylethayer",
    twitter_handle: "@kylemthayer",
    profile_picture: "kylethayer.jpg",
    follows: ["@SusanNotess", "@UW", "@UW_iSchool", "@ajlunited"]
  },
  {
    username: "Dr Susan Notess",
    twitter_handle: "@SusanNotess",
    profile_picture: "susannotess.jpg",
    follows: ["@kylemthayer", "@histoftech", "@j_kalla", "@dbroockman", "@qaxaawut", "@shengokai", "@laniwhatison"]
  },
]
```
````
