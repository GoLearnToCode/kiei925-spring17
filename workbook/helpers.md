# Cheat Sheet: View Helpers

In Rails-speak, *view helpers* are predefined methods that will generate HTML on our behalf.  You should always use these helper methods instead of writing the HTML yourself for the following reasons:

1. Your code will be easier to understand.
1. Your code will result in perfect HTML5-compliant code.
1. Your code will get some superpowers that "normal" HTML can't accomplish.

There are dozens of built-in helper methods in Rails, but here are the most essential ones.

### 1. `link_to`

HTML links look like this:

``` html
<a href="http://www.google.com">Click here to Google</a>

<a href="/movies/index">Click here to see the list of movies</a>
```

We can make our intentions a bit clearer by using the `link_to` helper:

``` erb
<%%= link_to "Click here to Google", "http://www.google.com" %>

<%%= link_to "Click here to see the list of movies", "/movies/index" %>
```

### 2. `image_tag`

When we want to embed a photo or image into our web page, there are two scenarios we have to consider, based on whether the photo lives on the internet somewhere, or whether we've put them into our project inside the `app/assets/images` folder.

For images that already have an internet url, it's pretty straightforward to write raw HTML (though we still don't recommend it):

``` html
<img src="http://url/to/photo.png">
```

For images that are contained inside of our `app/assets/images` folder, using the raw `<img>` tag is error-prone because of the way the Rails will generate public urls.  So we must use the `image_tag` helper in this case anyway.

Here's how you can use the `image_tag` helper to show images, regardless of whether you have a public url or an app-hosted image:

``` erb
<%%= image_tag "http://url/to/photo.png" %>

<%%= image_tag "photo.png" # uses /app/assets/images/photo.png %>
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
