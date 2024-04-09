# Basic Data Types

First, we'll look at a few basic data storage types. We'll also be including some code examples you can look at, though don't worry yet if you don't understand the code, since we'll be covering these in more detail throughout the rest of the book.

## Booleans (True / False)
Binary consisting of 0s and 1s make it easy to represent true and false values, where 1 often represents true and 0 represents false. Most programming languages have built-in ways of representing True and False values.

```{figure} dog_tweet_binary.png
---
name: tweet_binary_fig
alt: Screenshot of the tweet from before, but with the blue checkmark highlighted
---
A blue checkmark (at the time) was something an account either had or didn't have, so it can be stored as a binary value.
```


Booleans are often created when doing sort of comparison or test, like:
- Do I have enough money in my wallet to pay for the item?
- Does this tweet start with "hello" (meaning it is a greeting)?

````{admonition} Click to see example Python code
:class: dropdown
```python
# Save a boolean value in a variable called does_user_have_blue_checkmark
does_user_have_blue_checkmark = True

# Save a boolean value in a variable based on a comparison.
# The code checks if a wallet has more in it than the cost of the item
#   which will be True or False, and be saved in has_enough_money
has_enough_money = money_in_wallet > cost_of_item

# Save a boolean value in a variable based on a function call.
# The code checks if the text of a tweet (stored in tweet_text) starts
#   with "Hello", which will be True or False, and be saved in is_greeting
is_greeting = tweet_text.starts_with("Hello")
```
````

## Numbers
Numbers are normally stored in two different ways:
- Integer: whole numbers like 5, 37, -10, and 0
- Floating point numbers: these can represent decimals like: 0.75, -1.333, and 6.626 × 10 ^ −34 (see more about [the complications of floating point numbers in binary](https://jvns.ca/blog/2023/01/13/examples-of-floating-point-problems/) {cite:p}`evansExamplesFloatingPoint2023`)

```{figure} dog_tweet_with_numbers.png
---
name: tweet_numbers_fig
alt: "Screenshot of the tweet from before, but with the numbers highlighted: replies, retweets, likes"
---
The number of replies, retweets, and likes can be represented as integer numbers (197.8K can be stored as a whole number like 197,800).
```

````{admonition} Click to see example Python code
:class: dropdown
```python

# Save an integer value in a variable called num_tweet_likes
num_tweet_likes = 197800

# Save an integer value in a variable called max_tweet_length
max_tweet_length = 280

# Save a floating point number in a variable called average_tweet_length
average_tweet_length = 133.5
```
````

When computers store numbers, there are limits to how much space is can be used to save each number. This limits how big (or small) the numbers can be, and causes rounding with floating-point numbers.

Additionally, programming languages might include other ways of storing numbers, such as fractions, [complex numbers](https://en.wikipedia.org/wiki/Complex_number) {cite:p}`ComplexNumber2023`, or limited number sets (like only positive integers).



## Strings (Text)
Computers typically store text by dividing the text into __characters__ (the individual letters, spaces, numerals, punctuation marks, emojis, and other symbols). These characters are then stored in order and called __strings__ (that is a bunch of characters strung together, like in {numref}`birthday_string_fig` below).

```{figure} happy_birthday_banner.jpg
---
name: birthday_string_fig
alt: 'A photo of a string banner with shiny individual letters hanging on it spelling "HAPPY BIRTHDAY"'
---
A physical string of the characters: "H", "A", "P", "P", "Y", " ", "B", "I", "R", "T", "H", "D", "A", "Y". ([image source](https://www.pexels.com/photo/a-rocking-horse-and-birthday-decorations-7600328/))
```

In our example tweet, we can see some different pieces of information that might be represented with strings:

```{figure} dog_tweet_with_strings.png
---
name: tweet_strings_fig
alt: "Screenshot of the tweet from before, but with pieces of text highlighted: The user name, twitter handle, and the tweet text"
---
The user name, twitter handle, and the tweet text can all be represented with strings.
```


````{admonition} Click to see example Python code
:class: dropdown
```python
# Save a string in a variable called user_name
user_name = "WeRateDogs®"

# Save a string in a variable called twitter_handle
twitter_handle = "@dog_rates"

# Save a string in a variable called tweet_text
twitter_handle = "This is Woods. He’s here to help with the dishes. Specifically the pre-rinse, where he licks every item he can. 12/10"
```
````

Text can be stored with extra formatting information, such as fonts and colors, in different [document file formats](https://en.wikipedia.org/wiki/Document_file_format) {cite:p}`DocumentFileFormat2023` like Word Documents, PDF files, [html website files](https://www.w3schools.com/html/html_intro.asp) {cite:p}`IntroductionHTML`, etc.

Note: We'll demonstrate strings later in this chapter, and in more detail in Chapter 7: Trolling
