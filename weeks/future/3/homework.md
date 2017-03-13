# Due Before the Next Class

**Prep Work**

1. Before doing anything else, read through these instructions, and then jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
3. Create a new Cloud9 workspace:
  - Name it `hw3`.  
  - You can leave the Description field blank.
  - Use the **Clone from Git** option and specify ```http://github.com/kiei925-spring17/etsy3```
  - Select the **Ruby** template
  - Click "Create Workspace"
2. Once inside the `hw3` project, go to the Terminal window and run this command: `bundle`
3. Run the project and verify that you can view the home page in your browser.  You should be able to click on an item to get to its `show` page.
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).

**Contribute a Project Idea**

1. Go to [this Google Sheet](https://docs.google.com/spreadsheets/d/1TRq-u4ohBstllKNw_Hw11hlDhFhjmRPAzje9jaNnJZM/edit?usp=sharing) and add at least one project idea, hopefully two or three.  You're not obligated to build your idea as your final project.  This is just a brainstorming session for all of us.

**Create A Database-Backed Model**

1. Find the `db/models.yml` file and add two models: `Listing` and `Shop`.  Determine the attributes you will need for each model by reading the Business Rules section below.
2. Use the `rails console` in a Terminal window to add at least two shops and four products.  Use the `etsy-data.json` file as a guide, or make up your own products!  Each shop must have at least two listings for sale.
2. Modify the `index` view to be database-backed, by using the `Listing` model to help generate the HTML.  
2. Modify the `show` view to be database-backed, by using the `Listing` and `Shop` models to help generate the HTML.  
  - Display the name of the associated Shop in or near the title in the `h1` element.
  - Clicking the photo should no longer navigate to the real Etsy page.  (Instead, our app is finally becoming the "real" Etsy.)
  - Display a list of small, thumbnail images of all of listings in the same shop.
  - Clicking one of the thumbnail images should navigate directly to that listing's `show` page.

HINT: You should not have any references to the old `EtsyData` class anymore when you're done, nor should there be any direct links to etsy.com anymore.

HINT 2: Be insanely curious. I wrote a lot of code for you.  Prove
to yourself how everything you see in the browser has been made to appear.

**Final Step**

4. Do this last: somewhere on the home page, use HTML to display your estimate and actual time.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

---

**Business Rules**

1. Every shop must have a unique name.
1. Every listing must belong to a shop.
1. A listing has: a title, price, URL to a photo, URL to a real Etsy listing, and the number of users who have "favorited" it.
1. Prices must be stored in the database as an integer number of cents; for example, a price of $10.00 should be stored as the integer 1000.  When displayed to the user, prices should be formatted as a regular currency amount ("$10.00").
1. Listings should be identified by our database system, and will no longer reference the "real" Etsy listing id.

---

**GRADING**

- 3 points: Proper definitions for both models, at least 2 Shop rows created, each with at least 2 associated Listing rows.
- 3 points: Data-driven implementations of both `index` and `show` views, including displaying the shop name on the `show` page and thumbnail images of all of the shop's listings.
- 3 points: FREE because I originally wrote the wrong instructions here. :-)
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them) **AND** you have contributed at least one project idea to the Google Sheet.
