# Reading

* Don't forget about the Course Workbook, including lots of examples of how to <%= workbook_link "use the Rails console", :console_crud %>.
* Keep reading Getting Real.  Ponder user stories and business requirements, and think about how much you agree or disagree with what the book says.

# Week 3 Survival Guide

* We can store data in a relational database for our app to use.
* Each table in the database corresponds to a *model* in our application.
* Define your models in `db/models.yml` and then run `rake db:migrate` from a Terminal window.  You can change what's in the `models.yml` file as much as you want.  Just be sure to `rake db:migrate` from a Terminal after each change.
* Using Ruby, you can use your model to create new rows in your tables, read rows, update rows, and delete rows.  
* We can use Ruby code to add intelligence to our views.  A typical `if` statement looks like this:

``` ruby
# Note the double equal sign!
<%% if password == "swordfish" %>
  <p>You said the magic word!</p>
<%% end %>
```

* We can add intelligence to our controllers by defining controller methods:

``` ruby
class MoviesController < ApplicationController

  
end
```
