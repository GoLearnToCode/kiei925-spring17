# Due Before the Next Class

This is the last homework assignment of the quarter.  Isn't this sad? :-(

**Prep Work**

1. Before doing anything else, read through these instructions, and then jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
3. Create a new Cloud9 Ruby on Rails workspace named `hw5` based on ```http://github.com/kiei925-spring16/etsy5```
2. Once inside the `hw5` project, do whatever's necessary to get the app up and running.
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  

**Connect the Models**

Start by perusing the code that's already there.  Look at the routes, controllers, models, and views.  Notice the new `Shops` link in the navbar.



1. **Identify Associations**. Use `has_many` and `belongs_to` in your model files to build declarative relationships between them.

2. **Use Association Methods**.  Modify the views by removing as many queries as you can, and replacing them with association methods.  For example, instead of code like `Director.find_by(id: @movie.director_id)`, I could write `@movie.director` by first implementing the proper model associations.  Hint: There are queries that can be rewritten in the following actions: `shops#index`, `shops#show`, and `listings#show`.

*Just a reminder: from the user's point of view, the application behavior should not change.  Only the code.*

**Final Step**

3. Do this last: somewhere on the home page, use HTML to display your estimate and actual time.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.


**GRADING**

- 4 points: Proper implementation of association methods.
- 4 points: Applying association methods wherever possible.
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them).

