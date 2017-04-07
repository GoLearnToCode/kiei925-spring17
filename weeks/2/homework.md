# Due Before Next Class

**Part A: Preparation**


1. Before doing anything else, read through these instructions, and then jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
2. Go to etsy.com.  Pick two or three items to buy, and observe the URLs.  Notice how they named their resources (the items for sale).  (Hint: it's not _products_.)
3. Create a new Cloud9 workspace:
  - Name it `hw2`.  
  - You can leave the Description field blank.
  - Use the **Clone from Git** option and specify ```http://github.com/kiei925-spring17/etsy2```
  - Select the **Ruby on Rails** template
  - Click "Create Workspace"
2. Once inside the `hw2` project, go to the Terminal window and run this command: `bundle`
3. Run the project so that you can see the home page in your browser.  It should look like a simplified, static version of the Etsy home page.
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).


**Part B: Create A Data-Driven Resource**

1. Create a resource named `listings` (if you're not sure how to do that, you should read the cheat sheet <%= workbook_link 'Creating a New Resource', :resource %>).
2. Your `index` action (i.e. the url `/listings`) should show a list of items for sale.  
  - Your `index` page should still look looking exactly like the home page. But your HTML should be mixed with embedded Ruby code that uses the `Item` class.
  - See the 'Hints' section below for more information on how to use the `Item` class that I've prewritten for you.  
3. Clicking on an item's title or photo should navigate the browser to `/listings/{something}`, where `{something}` is the `sku` of the item that was clicked.
3. Support the following url: `/listings/{something}` and have it display the details page for the given listing.
  - Use the filename `show.html.erb`
  - It's your job to figure out what data is available to you from the `Item` model and display all of it on the page somewhere.  
  - For inspiration, take a look at a [real EtsyData listing page for inspiration](https://www.etsy.com/listing/471085558/walnut-bowl-w0481).  You need only create a _very, very simplified version_.  You do not need to worry about any fancy CSS.  
  - The primary goal is to make sure the data shown is correct for the given listing as shown in the URL address bar.
4. Modify your `routes.rb` so that your `index` page is also the home page.

**Final Step**

1. Do this last: somewhere on the home page, use HTML to display your estimate and actual time.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

**GRADING**

- 4 points: Data-driven implementation of `/listings`.
- 4 points: Data-driven implementation of `/listings/{something}`.
- 1 point: The view for `/listings` is also the home page.
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them).

**HINTS**

I've already written the layout file and the temporary `pages` resource for you.  That's how the home page initially works.  Use the static home.html.erb as a guide for what you need to implement in `/listings`.

I've also written a model for you named `Item`.  Here's how you can use it from your code:

1. `Item.all` will return an array of items. It's up to you try to discover the content and structure of the items (hint: use `rails console` to explore.).
2. `Item.find_by(sku: ...)` will return a single item whose `sku` column value matches the value you provide; i.e. `EtsyData.find_by(sku: "1234")` will retrieve the item with sku `1234`.
