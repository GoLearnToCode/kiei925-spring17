**Goals:**

- models
- console CRUD
- index and show page use database
- new hash syntax
- .find_by, .where, .order

**Prep:**

- from last week

Lecture:
  - how about those estimates?
  - What do you think of Getting Real so far?
  - Project Spreadsheet
  - Use the Workbook!!

Icebreaker Challenge:
  - ./catchup


Demo 1: Create a `Movie` and `Director` models
  - schema on chalk board
  - edit `db/models.yml`
  - `rake db:migrate`
  - `rails console` for `Movie.all` and `Movie.count`

Demo 2: Console CRUD
  - `.new`
  - `.save`
  - `.find_by` and `nil`
  - `.where`
  - `.order`

**BREAK**

Challenge: Use the database in the index page
  - talk through the index page first
  - rewrite index page

Challenge: rewrite show page

Demo 4: One-to-Many
  - Show director for a movie

Demo 5: Conditionals
  - do not show director line if director is nil


Unresolved Pain:
  - how do we add a new movie?
  - maybe wish for /movies/new - it's supported!
  - maybe add new.html.erb and provide a form?
