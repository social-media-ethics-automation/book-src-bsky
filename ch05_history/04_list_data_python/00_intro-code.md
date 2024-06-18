# Looping with Lists and Dictionaries in Social Media

We mentioned previously in chapter 4, we can use lists and dictionaries to represent social media data:

__Example list of dictionaries of user data__

User 1:
- Username: kylethayer (a String)
- Twitter handle: @kylemthayer (a String)
- Profile Picture:  (an image)
- Follows: @SusanNotess, @UW, @UW_iSchool, @ajlunited, ... (a list of Strings)

User 2:
- Username: Dr Susan Notess (a String)
- Twitter handle: @SusanNotess (a String)
- Profile Picture:  (an image)
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
  }
]
```
````

Now, in order for us to work with this kind of data, we need to look more at lists and dictionaries, as well as how to loop over them.

```{tableofcontents}
```
