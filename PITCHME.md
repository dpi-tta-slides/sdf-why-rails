---
marp: true
title: SDF Why Rails?
description: This lesson reviews the Rails doctrine
# theme: uncover
transition: fade
paginate: true
_paginate: false
---


- Did you know that the DNA of humans and chimpanzees is about 98% the same?
- Most of our DNA is the plumbing of being alive, being primates, etc.
- Only a tiny bit makes us distinct from chimpanzees.
- We have exactly the same 98% since we descended from a common ancestor, approximately 6-10 million years ago.

---

- Similarly, Twitter and Airbnb share 98% of their code.
- Most of any SaaS application are common plumbing: having a web server, connecting to the database, etc.
- Only a tiny bit makes them distinct from one another — tweets instead of listings, etc.
- Twitter and Airbnb, too, have exactly the same core code; since they too had a common ancestor.

---

- In 2003, a Chicago entrepreneur (Jason Fried) hired a Danish programmer (David Heinemeier Hansson) to build an idea he had for project management SaaS. They called it Basecamp.
- David loved an obscure programming language called Ruby, which was invented in Japan in the mid 1990’s. Ruby was slow, but expressive and “beautiful” (to David). Jason didn’t really care what David used so he said 👍

---

- Once he got Basecamp working, David extracted the 98% of it that was common plumbing for all SaaS and released it for free, open-source. He called this package of Ruby code that let you quickly get a web application up and running “Ruby on Rails.” It was, at the time, revolutionary.

- So this is going to be our hack:
- Much like Twitter, Airbnb, NYTimes, GitHub, and thousands of other companies, we’re going to borrow David’s (and, by now, thousands of other contributors’) code.
- This will let us skip re-inventing tens of thousands of lines of code and many years of learning.

---

We just need to learn enough of the Ruby language to be able to navigate Ruby on Rails, the framework. (“Framework” just means “a bunch of code we’re borrowing”.)
This will be our strategy. For example, we’ll learn just enough of another language, CSS, to be able to use a CSS framework called Bootstrap to make our pages look professional.
In general, we will stand on the shoulders of giants.

---

# Play the whole game (integrated systems)
- The crucial piece in finally making programming “click” is learning all the skills needed to deploy an application, not just one or two. I.e., we become full-stack developers.
- Most courses or books teach you one language or skill, but then you’re left wondering how that fits in with the 99 other things you need to know in order to deploy an application.
- Making a real, functional application is motivating! It gives you a reason to continue learning — to improve it, and to make the next one.

---

# Programmer Happiness

The Principle of Least Surprise
```
$ irb
irb(main):001:0> exit
$ irb
irb(main):001:0> quit

$ python
>>> exit
Use exit() or Ctrl-D (i.e. EOF) to exit
```

- Ruby accepts both exit and quit to accommodate the programmer’s obvious desire to quit its interactive console.
- Python, on the other hand, pedantically instructs the programmer how to properly do what’s requested, even though it obviously knows what is meant (since it’s displaying the error message).

---

# Convention over configuration

- decrease the number of decisions that a developer is required to make without losing flexibility


<!-- foreign key example -->
Who cares what format your database primary keys are described by? Does it really matter whether it’s “id”, “postId”, “posts_id”, or “pid”? Is this a decision that’s worthy of recurrent deliberation? No.

<!-- TODO: routing example -->




<!-- model example / folder structure -->
when you have a User model in your application, then Rails assumes that it is defined in the file at app/models/user.rb. If that is the case then you do not need to require that file before using and Rails' autoloading feature will be able to do that for you. And Rails will assume that the user records will be stored in a database table named users. If that is the case, no additional configuration will be needed and Rails will be able to load these records. But if the records are stored in a different table, then you will have to explicitly tell Rails the new table name.
