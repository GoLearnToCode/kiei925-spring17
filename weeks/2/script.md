**Goals:**

- resource routing
- index and show page
- arrays and hashes
- params hash
- rails console to see variables

**Demo 1: Resource Routing**

  - Go to `/cards`
  - How does that page show up?

**Demo 2: ERB**

  - Go to `/cards/index.html.erb`
  - Change the url to show different cards
  - Use a variable to hardcode a value or suit
  - Use ERB to plug that variable in

**Demo 3: .each**

  - Still inside `/cards/index.html.erb`
  - Use `.each` to show all 13 cards of the same suit
  - Use `.each` to show the entire deck


**BREAK**

**Demo 4: Intro to Console: .all and .find_by**
  - `Movie.all`
  - `Movie.find_by`

**Demo 5: Movies page**
  - Go to `/movies`
  - Demo: how is the current code working
  - LAB: Add another movie that you like (copy/paste entire section)
  - LAB: Show all the movies

**Demo 6: param["id"]**
  - Demo: how to use `params["id"]` inside `show.html.erb`
  - LAB: Challenge: show the correct movie


**Homework Preview**

? Identify resources on your favorite websites



Unresolved Pain:
  - how do we add a new movie?
  - maybe wish for /movies/new - it's supported!
  - maybe add new.html.erb and provide a form?
