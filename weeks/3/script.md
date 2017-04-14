**Goals:**

- root
- one-to-many
- foreign keys
- .where, .order
- .update
- nil
- if

**Prep:**

- ./catchup


**Start**

Lecture:
  - Use the Workbook!!

Demo 1: Home Page
  - `root`
  - CHALLENGE: Modify page header to link to home page

Demo 2: `Movie` and `Director` models
  - schema on chalk board
  - edit `db/models.yml` to add foreign key
  - `rake db:migrate`
  - `rails console` to `.create` a couple of directors
  - `.update` to connect a movie to a director
  - `show` page to show director's name (watch out for nil)

Demo 3: Conditional Logic
  - `.find_by` and `nil`
  - Do not show director if director is `nil`

**IF < 3:30pm**

Demo 4: many side
  - uncomment seeds file
  - director's show page
  - push & catchup
  - list films directed by that director

**BY 3:45**
Lecture:
  - User stories for Amazon
  - Final project

Unresolved Pain:
  - how do we add a new movie?
  - maybe wish for /movies/new - it's supported!
  - maybe add new.html.erb and provide a form?
