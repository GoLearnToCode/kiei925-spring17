# Reading


Watch the very short TED talk on this page: http://www.tomwujec.com/design-projects/marshmallow-challenge/

### Week 2 Survival Guide

Here's a quick cheat sheet to the various commands and concepts we covered in class.

* Ruby provides _hashes_ and _arrays_ just like JavaScript (but JavaScript calls them _objects_ and _arrays_).
* There are a couple of ways to experiment with Ruby.  One way is to use the **rails console** (start it from a Terminal window).  You can assign variables and try to make expressions.  Variable values are thrown away when you exit.  You can type **exit** when you're done.  
* Another way to experiment with Ruby is to embed Ruby code inside your HTML views.  Use `<%%= .... %>` to inject the result of any Ruby expression into your HTML. Or, just use `<%% ... %>` to "silently" evaluate Ruby code and assign variable values.
* Got a variable and need to know what kind of data it holds?  Use the `.class` method.  For example, `x.class` will tell you what type of data is inside the variable `x`.
* Add new resources with the `resources` route command.  For example: `resources "products"`
* The `resources` route command will activate several "actions" for your application.  The two most important (for now) are the `index` and `show` actions.  See the table below for examples.
* Use `params["id"]` to retrieve the second half of the URL.
* When you need to iterate over an array, use the `.each` method.

Here's an example that summarizes all of the above.  Given the following line in `routes.rb`:

``` resources :movies ```

we get two "actions" (an action is the triggering of an HTML template file):

|Action Name|URL Path|View File|
|----|------|--------|
|`index`|`/movies`|`app/views/movies/index.html.erb`|
|`show`|`/movies/:id`|`app/views/movies/show.html.erb`|

That `:id` is a placeholder, so that we can match the URL based on a _pattern_ rather than predefined, explicit numbers. We don't know what will be there until someone actually uses our website.  When someone does try to go that page (i.e. `/movies/5`), our code can use the `params` hash to "grab" the actual value from the address bar:


```
<p>You are trying to view the movie identified by: <%%= params["id"] %></p>
```
