# Due Before Next Class

**Prep Work**


1. Before doing anything else, read through these instructions, and then jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
2. Go to etsy.com and browse around a bit as if you're trying to buy something, paying attention to the URLs they use.  Pick two or three items to buy, and observer the URLs.  They decided not to refer to the items for sale as _products_, but instead as something else - can you figure out what term they like to use?
3. Create a new Cloud9 workspace:
  - Name it `hw2`.  
  - You can leave the Description field blank.
  - Use the **Clone from Git** option and specify ```http://github.com/kiei925-winter17/etsy2```
  - Select the **Ruby on Rails** template
  - Click "Create Workspace"
2. Once inside the `hw2` project, go to the Terminal window and run this command: `bundle`
3. Run the project so that you can see the home page in your browser.  It should look like a simplified, static version of the Etsy home page.
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).


**Create A Data-Driven Resource**

1. Create a resource named `listings` (if you're not sure what that means, go read <%= workbook_link 'Creating a New Resource', :resource %>).
2. Support the `index` action (the url `/listings`) by using the `Etsy` data class to help generate the HTML.  
  - It should end up looking exactly like the home page, but your HTML should be generated as much as possible by embedded Ruby code that uses the `Etsy` class.
  - See the 'Hints' section below for more information on how to use the `Etsy` class that I've prewritten for you.  
3. Clicking on an item's title or photo should navigate the browser to `/listings/{something}`, where `{something}` is the `listing-id` of the item that was clicked.
3. Support the following url: `/listings/{something}` and have it display the details page for the given listing.
  - It's your job to figure out what data is available to you from the `Etsy` class and display all of it on the page somewhere.  
  - Look at a [real Etsy listing page for inspiration](https://www.etsy.com/listing/244820198/walnut-bowl-w0162), but you need only create a _very, very simplified version_.  You do not need to worry about any fancy CSS.  
  - The main idea is to make sure the data shown is correct for the given listing as shown in the URL address bar.
  - Clicking on the photo should take the user to the real Etsy listing page.
4. Rewrite the route for the home page so that the same view you used for `/listings` is also used as the home page.  

**Final Step**

4. Do this last: somewhere on the home page, use HTML to display your estimate and actual time.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

**GRADING**

- 2 points:  Proper route for a `listings` resource.
- 3 points: Data-driven implementation of `/listings`.
- 3 points: Data-driven implementation of `/listings/{something}`.
- 1 point: The view for `/listings` is also the home page.
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them).

**HINTS**

I've already written the layout file and the `pages` resource for you.  That's how the home page initially works.  Use the static home.html.erb as a guide for what you need to implement in `/listings`.

I've also written a data class for you named `Etsy`.  Here's how you can use it from your code:

1. `Etsy.all` will return an array of items. It's up to you try to discover the content and structure of the items.
2. `Etsy.find(something)` will return a single item whose listing-id matches the value you pass for `something`, i.e. `Etsy.find(1234)` will retrieve the data for listing #1234 (if that listing exists).
3. The `Etsy` data class doesn't really connect to Etsy.com; it only knows the information for 4 specific listings.

