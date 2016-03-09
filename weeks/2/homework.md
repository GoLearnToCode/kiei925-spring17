# Due Before Next Class

If you haven't already, do the interactive Ruby tutorial at [tryruby.org](http://tryruby.org)

1. Create a new C9 workspace called `poker` and specify the following Git clone url: `http://github.com/kiei925-spring16/newapp`. 
2. In your Rails app, your home page should show a randomly-dealt hand of cards.  Each time you refresh the page, a new hand of cards should appear.
3. Display the cards as images.  

**HINTS**

I've made a full deck of nice images available for you.  There are 52 images and the names of the URLs follow a particular pattern, so that your code can guess the right filename.  Here's the pattern:

```http://golearntocode.com/images/cards/{number}_of_{suit}.png```

For example:

```http://golearntocode.com/images/cards/10_of_diamonds.png``` 

is the image for the 10 of diamonds:

![Card](http://golearntocode.com/images/cards/10_of_diamonds.png)
