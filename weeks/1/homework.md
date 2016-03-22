# Homework #1: Due Before the Next Class

1. Before doing anything else, first jot down how long you estimate it will take you to do this homework, and try to keep track of how much time you spend on the homework this week.
2. Install the following Chrome Extensions: _ColorZilla_, _JSONView_, and _WhatFont_
1. Draw a wireframe of a simplified version of Etsy.com's home page.  Take a picture of it.
3. Create a new Cloud9 workspace named `hw1` and use the option to clone ```http://github.com/kiei925-spring16/etsy1```. 
2. In your Rails project, replace the default home page with one based on your wireframe.
3. Upload your wireframe into your project. Save it into your project as `wireframe.png` (or some other image format).
4. Do this last: somewhere on your home page, use HTML to display your estimate and actual time; for example:

``` html
<p><small>I originally estimated 2 hours. It actually took me 12 hours.</small></p>
```
Of course, use your own values instead of the numbers shown above.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

**GRADING**

- 7 points:  A Rails application whose home page shows a simplified version of the Etsy home page.  Grading is based mostly on mechanics ("does it show a web page"), but decent CSS styling is expected.
- 2 points: An uploaded wireframe.
- 1 point: The home page includes your estimate and actual.

**HINTS**

- The application layout file is `app/views/layouts.html.erb`
- Your css goes in `app/assets/stylesheets/application.css` after all of the comments
- You will need a Rails controller to represent your home page:
    - Create a file named `app/controllers/pages_controller`
    - Peek at the code we wrote in class for an example of the Ruby code in your controller file
    - Create a folder named `app/views/pages`
    - Create a file named `app/views/pages/home.html.erb` to contain your HTML code
    - Create a route in `config/routes.rb`: `root 'pages#home'` so that Rails will use your page as the new home page
    

    




