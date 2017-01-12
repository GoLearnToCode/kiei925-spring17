Goals:

- resource routing
- index and show page
- arrays and hashes
- params hash
- rails console to see variables

Prep:

- in-class app should have one finished resource (routes and just index page)  
- in-class app should have one broken resource: routes and controller missing, index.html.erb prewritten but unreachable
- index.html.erb should be a hardcoded series of `find` + markup to display a few items

Lecture:
  - your app is just a container of resources
  - the web is organized by resource locators

Icebreaker Challenge

- fix broken resource to see index page?

Demo 1:
  - rails console to `find` an item
  - ruby hashes
  - try to pull specific values out of the hash

Demo 2:
  - resource 'movies' also allows for `/movies/:id`
  - EDD: try to browse for a specific item
  - server log discovery
  - show.html.erb with hardcoded item
  - Challenge: use params hash to display the right movie

Demo 3:
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
