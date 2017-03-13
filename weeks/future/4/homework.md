# Due Before the Next Class

**Prep Work**

1. Before doing anything else, read through these instructions, and then jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
3. Create a new Cloud9 workspace:
  - Name it `hw4`.  
  - You can leave the Description field blank.
  - Use the **Clone from Git** option and specify ```http://github.com/kiei925-winter17/etsy4```
  - Select the **Ruby on Rails** template
  - Click "Create Workspace"
2. Once inside the `hw4` project, go to the Terminal window and run these commands:
  - `bundle`
  - `rake db:migrate`
  - `rake db:seed`
3. Run the project and verify that you can view the home page in your browser.  You should be able to click on an item to get to its `show` page.
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).

**Create A Full Database-Backed Resource**

Start by perusing the code that's already there.  Look at the routes, the Listings controller, and the views.

Your job is to modify the `Listings` resource (controller and views) so that users can view, add, delete, and update everything.

1. **CREATE**. On the listings page (`index`) add a link that says "Add New Listing".  This link should navigate to `/listings/new` which should display a form using the `bootstrap_form_for` structure.  Users should be able to complete the form and click a Submit button, which should add the new listing to the database and redirect the user back to the listings page.
2. **READ**.  Allow users to view all listings as well as the details for a single listing.  This has already been completed for you! Woohoo! :-)
3. **UPDATE** From the details page of a listing, add a link that says "Edit This Listing."  This link should navigate to `/listings/:id/edit`, where `:id` is the database `id` of the listing.  The view should be called `edit.html.erb`, and it should display form that is prefilled with data from the listing.  Users should be able to complete the form and click a Submit button, which should update the appropriate listing in the database, and then (finally) redirect the user back to the `show` page for that listing. (It's your job to figure out how to receive the form submission, update the appropriate row in the database, and then redirect).
3. **DELETE** From the details page of a listing, add a link that says "Delete This Listing."  This link should trigger a controller action named `destroy`, which should delete the listing from the database.  It should also redirect the user back to the `index` page. (HINT: you'll need to use the `<%%= link_to ....., method: :delete %>` syntax in order to properly trigger the `destroy` action.

*Just a reminder: you are only required to modify the Listing resource.  You don't need to add/edit/delete any Shop rows.*

**Final Step**

4. Do this last: somewhere on the home page, use HTML to display your estimate and actual time.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.


**GRADING**

- 3 points: Proper implementation of the **CREATE** step.
- 3 points: Proper implementation of the **UPDATE** step.
- 3 points: Proper implementation of the **DELETE** step.
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them).
