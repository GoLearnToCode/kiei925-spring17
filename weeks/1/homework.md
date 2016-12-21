# Homework #1: Due Before the Next Class

**Please follow these instructions as carefully as possible**

1. Before doing anything else, first jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
2. Install the following Chrome Extensions: _ColorZilla_, _JSONView_, and _WhatFont_
1. Draw a wireframe of a simplified version of Etsy.com's home page.  Think about a _minimal home page_, the core offering, and the simplest implementation necessary to gain traction. Take a picture of your wirefame.
3. Create a new Cloud9 workspace:
  - Name it `hw1`.  
  - You can leave the Description field blank.
  - Use the **Clone from Git** option and specify ```http://github.com/kiei925-winter17/etsy1```
  - Select the **Ruby on Rails** template
  - Click "Create Workspace"
2. Once inside the `hw1` project, go to the Terminal window and run this command: `bundle install`
3. Finall, the fun part: replace the default home page with your own, based on your wireframe (see hints below).  Your finished HTML does not need to exactly match your wireframe, but it should be obvious that the wireframe guided your implementation.
3. Upload your wireframe into your project. Save it into your project as `wireframe.png` (or some other image format).
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).
4. Do this last: somewhere on your home page, use HTML to display your estimate and actual time; for example:

``` html
<p><small>I originally estimated 2 hours. It actually took me 12 hours.</small></p>
```
Of course, use your own values instead of the numbers shown above.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

**GRADING**

- 7 points:  A Rails application whose home page shows a simplified version of the Etsy home page.  Grading is based mostly on mechanics ("does it show a web page"), but decent CSS styling is expected.
- 2 points: An uploaded wireframe.
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them).

**HINTS**

- The application layout file is `app/views/layouts.html.erb`
- Your css goes in `app/assets/stylesheets/application.css` after all of the comments
- You will need a Rails controller to represent your home page:
    - Create a file named `app/controllers/pages_controller`
    - Peek at the code we wrote in class for an example of the Ruby code in your controller file
    - Create a folder named `app/views/pages`
    - Create a file named `app/views/pages/home.html.erb` to contain your HTML code
    - Peek at the code we wrote in class for an example of how to create a route in `config/routes.rb`
