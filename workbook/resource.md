# Creating a New Resource

In Rails, we embrace the idea that every web application is simply a container of _resources_.  Every web page belongs to a resource of some kind. 

A resource is:

* Something a user finds valuable.  _Examples: a product for sale, a movie review, an airline reservation, a photo of your friend's cat._
* A reason a user visits your site. _Examples: the latest baseball scores, the current weather, the latest photo of your friend's cat._
* A single item, or a classification of items. _Examples: the shuttle bus schedule, a product catalog, a photo of your friend's cat._

You must think of the resources that you're offering to your users.

Then, you can build those resources in code.  Here's how to build a single resource.

For this example, we pretend that we are building [IMDB](http://imdb.com).

STEP 0: Pick a Name for Your Resource

IMDB has lots of resources: movies, reviews, users, actors, directors, showtimes, ....

Let's start with _movies_. We use the plural form, _movies_, not the singular _movie_, when we're talking about resources.


STEP 1: The Route

In your config/routes.rb file:

`resources :movies`

This will allow your users to access a list of movies at `http://yourdomain.com/movies`.  Try it now.  

Did you get a big red error message complaining about an "uninitialized constant"?  That's good. You're ready for Step 2.

STEP 2: The Controller

Every resource needs a controller, which consists of a controller class and a folder to contain the HTML files for the resource. 

For the controller class, add a new file to your project named:

`app/controllers/movies_controller.rb`

Next, add a folder named:

`app/views/movies`

Finally, go back into app/controllers/movies_controller.rb and add this code:

```
class MoviesController < ApplicationController

end
```

Try refreshing your browser. You should see a big error message saying something about a "missing template". That's good! It means it's time for Step 3.

STEP 3: The View

When we add the route `resources :movies`, we actually promised a resource named `movies` (which we now have) and an HTML file named `app/views/movies/index.html.erb` which we don't have yet. So add a file by that name, and add this code into it:

<h1>Movies</h1>

Try refreshing your browser once more for `/movies`. You should see "Movies" in big, bold letters. If not, read the error message as best you can and review the steps above.

