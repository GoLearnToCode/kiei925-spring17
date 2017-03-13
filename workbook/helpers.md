# Cheat Sheet: View Helpers

In Rails-speak, *view helpers* are predefined methods that will generate HTML on our behalf.  You should always use these helper methods instead of writing the HTML yourself for the following reasons:

1. Your code will be easier to understand.
1. Your code will result in perfect HTML5-compliant code.
1. Your code will get some superpowers that "normal" HTML can't accomplish.

There are dozens of built-in helper methods in Rails, but here are the most essential ones.

### 1. `link_to`

Plain HTML links look like this:

``` html
<a href="http://www.google.com">Click here to Google</a>

<a href="/movies/index">Click here to see the list of movies</a>
```

We can use Ruby to make the code bit clearer by using the `link_to` helper:

``` erb
<%%= link_to "Click here to Google", "http://www.google.com" %>

<%%= link_to "Click here to see the list of movies", "/movies/index" %>
```

### 2. `image_tag`

When we want to embed a photo or image into our web page, there are two scenarios we have to consider, based on whether the photo lives on the internet vs. inside our `app/assets/images` folder.

For images that already exist on the internet, it's pretty straightforward to write raw HTML:

``` html
<img src="http://url/to/photo.png">
```

For images that are placed inside of our `app/assets/images` folder, we cannot use the HTML `<img>` tag.  We must use the `image_tag` helper function instead.


``` erb
<%%= image_tag "photo.png" # expects /app/assets/images/photo.png %>
```

### 3. `pluralize`

This code:

``` erb
<p>We have <%%= pluralize(2, "student") %> in this class.</p>
<p>You have <%%= pluralize(1, "message") %> waiting.</p>
```

will result in:
``` html
<p>We have <%= pluralize(2, "student") %> in this class.</p>
<p>You have <%= pluralize(1, "message") %> waiting.</p>
```
