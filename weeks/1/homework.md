# Homework #1: Due Before the Next Class

1. Before doing anything else, first jot down how long you estimate it will take you to do this homework, and try to keep track of how much time you spend on the homework this week.
2. Read the Etsy user stories and business rules.
2. Install the following Chrome Extensions: _ColorZilla_, _JSONView_, and _WhatFont_
1. Draw a wireframe of a simplified version of Etsy.com's home page.
3. Create a new Cloud9 workspace named `hw1` and select the option to clone ```http://github.com/kiei925-spring16/etsy1```. 
2. In your Rails project, replace the home page with a web page based on your wireframe.
3. Upload your wireframe (take a picture of it, etc.) and save it into your project as `wireframe.png` (or some other image format).
4. Now that you're finished: somewhere on your home page, use HTML to display your estimate; for example:

```html
<p><small>I originally estimated 2 hours. It took me 12 hours.</small></p>
```

Of course, use your own values instead of the numbers shown above.

**HINTS**

- The application layout file is `app/views/layouts.html.erb`
- Your css goes in `app/assets/stylesheets/application.css` after all of the comments
- You will need a Rails controller to represent your home page:
    - Create a file named `app/controllers/pages_controller`
    - Refer to the class code for an example of the Ruby code you'll need in your controller file
    - Create a folder named `app/views/pages`
    - Create a file named `app/views/pages/home.html.erb` to contain your HTML code
    - Create a route in `config/routes.rb`: `root 'pages#home'` so that Rails will use your page as the new home page
    

    




