# Due Before the Next Class

This is the last homework assignment of the quarter.  Isn't this sad? :-(

**Prep Work**

1. Before doing anything else, read through these instructions, and then jot down how long you estimate it will take you to do this homework. Keep track of how much time you spend on the homework this week.
3. Create a new Cloud9 Ruby workspace named `project` based on ```https://github.com/kiei925-winter17/starting-point```
2. Run `bundle` to make sure your workspace is ready for Rails
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  

**Sketch Your Domain Model**

1. **models.yml**.  Think about your models and the foreign keys you will
need to tie them together.  Use the proper naming conventions.  Run `rake db:migrate` and repeat as often as necessary.

2. **Apply Association Methods**.  Go into your models and add `has_many`,
`belongs_to`, and `has_many... :through...` declarations to affirm
the associations implied by your foreign keys.

3. **seeds.rb**.  Write a `seeds.rb` file that creates enough rows of data
for each model so that you can sufficiently test out your domain model.
Include code in your seeds.rb to delete all previous data first.

4. **README.md**.  Use Markdown formatting to write an overview of
your project.  Your overview should include:

* Your elevator pitch (1 paragraph max)
* User stories for the primary use cases (generally 8-12 stories)


**Final Step**

3. Do this last: somewhere on the home page, use HTML to display your estimate and actual time.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.


**GRADING**

- 6 points: Proper modeling (2 pts each for: proper column naming, association
  methods, and a sufficient seeds file).
- 3 points: Clearly written elevator pitch and properly formatted user stories.
- 1 point: The home page includes your estimate and actual. (Remember, your time values are not graded; you get a point for simply including the proper HTML to display them).
