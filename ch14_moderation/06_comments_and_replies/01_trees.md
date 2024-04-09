# Tree Structures

Let's look at an example of a comment with replies, and replies to those replies, etc. (this could be on twitter or any other social media system):

```{figure} comments_and_replies.png
---
name: comments_and_replies_fig
width: 300px
alt: "Initial comment: \"That last exam sure was hard!\" Two main replies, the first is \"It sure was hard, what score did you get?\" and that replies has two replies: \"I got a 67% :(\" and \"I got a 73%\". The second main reply is \"I didn't think it was that bad\". That second main reply has two replies, the first is \"how was that not a super hard exam?\" and the second is \"of course you didn't\", which has a reply \"what's that supposed to mean?\" which has a reply \"you're an overacheiver\" which has a reply \"and that's bad how?\""
---
A comment with replies.
```

Seeing comments and replies like this is hopefully familiar to you.

Let's look at this organized in a different organization, which is called a "tree" structure in programming and in math:

```{figure} comments_replies_trees.png
---
name: comments_replies_trees_fig
alt: "The same comments and replies as before, but organized into levels (the initial comment is level 1, the two main replies are level 2, the replies to those are level 3, etc.)"
---
A "tree" of comments and replies and replies to those.
```

In the "tree" structure, each comment or reply is called a "node," with the initial comment being the "root node." Each of these nodes has lines showing which nodes are replies (in math terminology the replies are "children").

So given this tree structure, how do we represent it in code, and how do we navigate it?
