# Tech Set-Up

## Hypothes.is Commenting

We recommend making a new **[private group](https://hypothes.is/groups/new)** on hypothes.is for the commenting system for each class, so the members of the class can see what others in the class think, and the students comments are private and not publicly available online. 

## Running Code
In order to run the code examples and do the code exercises in this book, here are some options:
1. You can use the rocket "Launch" button at the top of the page and open the file in Binder.
2. To run them on your own computer, you can download the JupyterNotebook (.ipynb files) and use a program like [Anaconda](https://www.anaconda.com/download). To find the relevant files, go to [the book_contents section](https://github.com/social-media-ethics-automation/book/tree/main/book_contents) of the github repository. From there you can go into the chapter you want, or "appendix" where teaching resources including the assignments (and helper files) are. You may also want to go to the fake_apis folder to get the testing version of the social media libraries.
3. To share a Jupyter Notebook environment with students, you can use [JupyterHub](https://jupyter.org/hub) (get the files the same way as above).

An additional note: It may be helpful to store your bot keys in their own separate file. For example: 
`reddit_keys.py`
```
username=""
password=""
client_id=""
client_secret=""
```
or

`discord_keys.py`
```
discord_token=""
```

Then in your JupyterNotebook files, you can include it by including this line:
```
%run reddit_keys.py
```

or
```
%run discord_keys.py
```