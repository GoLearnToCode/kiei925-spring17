# Goals

* Learn how to "CRUD" via the browser
* Learn how to implement resource-based routing (aka REST) in practice
* Mastery of `find_by`, `where`, `count`, `order` and `pluck`
* Learn about Rails' DSL for associating models: `has_many` and `belongs_to`

[Bootstrap forms documentation](https://github.com/bootstrap-ruby/rails-bootstrap-forms)


* We can use Ruby code to add intelligence to our views.  A typical `if` statement looks like this:

``` ruby
# Notice the double equal sign!
<%% if password == "swordfish" %>
  <p>You said the magic word!</p>
<%% end %>

# Notice the strange != sign!
<%% if password != "swordfish" %>
  <p>Nah-ah-ah! You didn't say the magic word!</p>
<%% end %>
