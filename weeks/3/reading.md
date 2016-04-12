# Reading

* Don't forget about the Course Workbook, especially <%= workbook_link "Intro to Domain Modeling", :domain_modeling %> and the exhaustive guide to <%= workbook_link "using the Rails console", :console_crud %>.
* Keep reading _Getting Real_.  Ponder user stories and business requirements, and think about how much you agree or disagree with what the book says.

# Week 3 Survival Guide

* We can store data in a relational database for our app to use.
* Using Ruby, you can use your model to create new rows in your tables, read rows, update rows, and delete rows.  
* We don't query the database directly. Instead, each table in the database corresponds to a Ruby *model* in the application.
* All model class names start with a capital letter, e.g.: `Movie`, `Director`, `Studio`, `Actor`.  
* You define your model data definition by filling out `db/models.yml` and then running `rake db:migrate` from the Terminal window. You can change what's in the `models.yml` file as much as you want.  Just be sure to `rake db:migrate` from a Terminal after each change.
* Each column will correspond to an object attribute that you can retrieve using `dot notation`, i.e. `m.title` where `m` is a variable of the `Movie` class; in other words, it represents a single row from our `movies` database table.
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

  def show
    if params[:id] == "123"
      redirect_to "http://www.google.com"
    end
  end

end
```
