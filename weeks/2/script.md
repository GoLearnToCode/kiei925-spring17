Goals:

- resource routing
- index and show page
- arrays and hashes
- params hash
- rails console to see variables

Prep:

- in-class app should have one finished resource (routes and just index page)  
- in-class app should have one broken resource: routes and controller missing, index.html.erb prewritten but unreachable
- prewritten index.html.erb should be a hardcoded series of `find` + markup to display a few items

Lecture:
  - your app is just a container of resources
  - the web is organized by resource locators

Icebreaker Challenge

- fix broken resource to see index page?
- study the index page - can you get a sense of how it works?

Demo 1: Recreate index page logic inside the console
  - rails console to `find` an item
  - ruby hashes
  - try to pull specific values out of the hash

Demo 2: EDD for show page
  - resource 'movies' also allows for `/movies/:id`
  - EDD: try to browse for a specific item
  - server log discovery
  - show.html.erb with hardcoded item
  - Challenge: use params hash to display the right movie

Demo 3: Pure Data-Driven Site
  - rails console to get a list of all items
  - rewrite index page with .each
    - first use variable `movie` many times
    - Force HTML to be identical for each movie
    - Notice what's changing, and what's constant
    - use .each to be lazy
    - Discover all the new items!



Unresolved Pain:
  - how do we add a new movie?
  - maybe wish for /movies/new - it's supported!
  - maybe add new.html.erb and provide a form?
