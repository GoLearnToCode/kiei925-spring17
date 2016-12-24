# Reading

Please read the following three articles this week. 

* [Introduction to User Stories](http://en.wikipedia.org/wiki/User_story)
* [Advantages of the User Story Template](http://www.mountaingoatsoftware.com/blog/advantages-of-the-as-a-user-i-want-user-story-template)
* [User Stories are not Requirements](http://www.scrumalliance.org/community/articles/2010/april/new-to-user-stories)

And then watch the very short TED talk on this page: http://www.tomwujec.com/design-projects/marshmallow-challenge/

### Week 2 Survival Guide

Here's a quick cheat sheet to the various commands and concepts we covered in class.

* There are a couple of ways to experiment with Ruby.  One way is to use the **rails console** (start it from a Terminal window).  You can assign variables and try to make expressions.  Variable values are thrown away when you exit.  You can type **exit** when you're done.  
* Another way to experiment with Ruby is to embed Ruby code inside your HTML views.  Use `<%%= .... %>` to inject the result of any Ruby expression into your HTML. Or, just use `<%% ... %>` to "silently" evaluate Ruby code and assign variable values.
* Got a variable and you want to know what type of data it holds?  Use the `.class` method.  For example, `x.class` will tell you what type of data is inside the variable `x`.
* Add new resources with the `resources` route command.  For example: `resources :products`
* The `resources` route command will activate several URLs for your application.  The two most important for now are the "index" and "show" routes.  See the table below for examples.
* Use `params["id"]` to "grab" the second half of the "show" route.
* Ruby provides _hashes_ and _arrays_ just like Javascript.
* When you need to iterate over an array, use the `.each` method.

Here's an example that summarizes all of the above.  Given the following line in `routes.rb`:

``` resources :movies ```

we get two "actions" (an action is a URL-to-HTML connection):

|Action Name|URL Path|View File|
|----|------|--------|
|index|`/movies`|`app/views/movies/index.html.erb`|
|show|`/movies/:id`|`app/views/movies/show.html.erb`|

That `:id` is a placeholder, so that we can match the URL based on a _pattern_ rather than predefined, explicit characters. we don't know what will go there at the time we write our code.  When our page is actually displayed for a particular user, we can use the `params` hash to "grab" the actual value from the address bar:


```
<p>You are trying to view the movie identified by: <%%= params["id"] %></p>
```
