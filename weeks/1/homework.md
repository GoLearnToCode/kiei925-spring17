# Homework #1: Due Before the Next Class

Please follow these instructions carefully.

**Part A: Preparation**

1. Before doing anything else, read through all of these instructions and jot down how long you estimate it will take you to do this homework. Then keep track of how much time you actually spend on the homework this week.
2. Install the following Chrome Extensions: _ColorZilla_ and _WhatFont_

**Part B: Read It**

(Estimated total reading time: 20 minutes)

* [Introduction to User Stories](http://en.wikipedia.org/wiki/User_story)
* [Advantages of the User Story Template](http://www.mountaingoatsoftware.com/blog/advantages-of-the-as-a-user-i-want-user-story-template)

**Part C: Build It**

Hop into your time machine.  It's 2005 and Etsy doesn't exist.  Let's build it ourselves and get rich!  

For this assignment we will just build the home page of our new site.  Think carefully about what we would need on our _minimal home page_.

What's our core offering?

What's the simplest implementation you can think of that would test our theory that customers are interested in handmade items?

If you look at Etsy.com's home page today, it's not minimal at all. That's because what we see today isn't what they started with.  This assignment challenges you to imagine what it might have looked like when they first launched.


1. Create a new Cloud9 workspace:
  - Name it `hw1`.  
  - You can leave the _Description_ field blank.
  - Use the **Clone from Git** option and specify `http://github.com/kiei925-spring17/etsy1`
  - Select the **Ruby** template
  - Click "Create Workspace"
2. Once inside the `hw1` project, go to the Terminal window and run this command: `bundle install`
3. Click the green **Run** button (or use the menu `Run > Run With > Ruby on Rails (stable + Ruby 2.2)`)
4. Get the application running in your browser.  You should see a temporary home page.
5. Replace the built-in home page with your own code, based on your wireframe (see hints below).  Your finished HTML does not need to exactly match your wireframe.
6. Try to match the fonts and colors that you see on the real Etsy.com website.
7. Change the HTML in the application layout file so that the browser displays "Etsy" in the browser's tab.
8. Somewhere on your home page, use HTML to display your estimate and actual time; for example:
``` html
<p><small>I originally estimated 2 hours. It actually took me 12 hours.</small></p>
```
Of course, use your own values instead of the numbers shown above.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

**PART D: Turn It In**

1. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).


**GRADING**

- 5 points:  A home page showing a simplified version of an Etsy-style home page.  
- 3 points:  Decent visual styling that roughly matches Etsy.com
- 1 point:  Correct browser tab title ("Etsy")
- 1 point: The home page includes your estimate and actual time. (The time values are not graded. You get a point for simply including the proper HTML to display them).

**HINTS**

- Your application layout file is `app/views/layouts.html.erb`
- Your css goes in `app/assets/stylesheets/application.css` after all of the comments
- Watch your server log for interesting things!  We will learn more about it next week.
